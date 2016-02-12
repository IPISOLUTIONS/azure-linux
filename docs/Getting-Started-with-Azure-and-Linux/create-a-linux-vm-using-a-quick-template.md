<properties
	pageTitle="Create a Linux VM using a quick template | Microsoft Azure"
	description="Create a Linux VM on Azure using a quick template."
	services="virtual-machines"
	documentationCenter=""
	authors="vlivech"
	manager="timlt"
	editor=""
	tags="azure-service-management,azure-resource-manager" />

<tags
	ms.service="virtual-machines"
	ms.workload="infrastructure-services"
	ms.tgt_pltfrm="vm-linux"
	ms.devlang="na"
	ms.topic="article"
	ms.date="12/15/2015"
	ms.author="v-livech"/>

# Create a Linux VM using a quick template

Templates allow you to create VMs on Azure with settings that you want to customize during the launch, things like usernames and hostnames.  For this article we will focus on launching an Ubuntu VM using a quick template that is on Azure repo on GitHub.

## Goal

- Clone Azure Quickstart Templates from Github
- Edit the Ubuntu 'simple linux VM' template
- Launch a new VM using that template

## Prerequisites

- An Azure account. [Get a free trial.](https://azure.microsoft.com/pricing/free-trial/)
- A Github account.
- An Azure Resource Group to launch the VM into

## Introduction

Cloud Templates use json files to instruct Azure on how to build your new VM with the settings you have chosen and written in the template file.  Templates can be used for simple one off tasks like launching an Ubuntu VM like we will do in this article.  Templates can also be used to construct complex Azure configurations of entire environments like a testing, dev or produciton deployment from the networking to the OS.

## Quick Commands

_Seasoned Linux Admins who just want the TLDR version start here.  For everyone else that wants the detailed explanation and walk through skip this section._

## Detailed Walk Through

Clone the Azure QuickStart Templates repo to your workstation.  Once it is cloned:

```
woz@macbook$ cd 101-vm-simple-linux
```

Now edit the `azuredeploy.parameters.json` file to change the Ubuntu settings to your own configuration:

_The `UbuntuOSVersion` calls for Ubuntu 14 LTS which is fine for this walk through and can be left unchanged._

```
woz@macbook$ vim azuredeploy.parameters.json

# Change anything <example> to your own settings

{
  "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentParameters.json#",
  "contentVersion": "1.0.0.0",
  "parameters": {
    "adminUsername": {
      "value": "<exampleUsername>"
    },
    "adminPassword": {
      "value": "<examplePassword>"
    },
    "dnsLabelPrefix": {
      "value": "<exampleDNSLabel>"
    },
    "ubuntuOSVersion": {
      "value": "14.04.2-LTS"
    }
  }
}
```

Run this command to launch the VM using that local template

_replace <example> with your own settings_

```
# Example Command
woz@macbook$ azure group create -n <exampleRGname> -l <exampleAzureRegion> azuredeploy.json -e azuredeploy.parameters.json

# Full command
woz@macbook$ azure group create -n simpleUbuntu -l westus azuredeploy.json -e azuredeploy.parameters.json
```

This will use the `azuredeploy.parameters.json` file that we edited to create a Resource Group with a single Ubuntu VM inside of it.

Templates can also be called from URLs, like this example that uses the same files as the last example but these are now in a repo on Github.  Make sure to use the raw links to the json files.

```
# Example Command
woz@macbook$ azure group create -n <exampleRGname> -l <exampleAzureRegion> --template-uri <https://raw.githubusercontent.com/repo/template.json> -e  <https://raw.githubusercontent.com/repo/template.parameters.json>

# Full Command
woz@macbook$ azure group create -n simpleUbuntu -l westus --template-uri https://raw.githubusercontent.com/vlivech/UbuntuVMTemplate/master/azuredeploy.json -e https://raw.githubusercontent.com/vlivech/UbuntuVMTemplate/master/azuredeploy.parameters.json
```
