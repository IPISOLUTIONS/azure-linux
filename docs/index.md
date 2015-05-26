Linux and Open-Source Computing on Azure
========================================

This document attempts to list in one place all the topics written by Microsoft and its partners about running Linux-based Virtual Machines as well as other open-source compute environments and applications on Microsoft Azure. As both Azure and the open-source computing world are fast-moving targets, it is almost certain that this document is out of date, *despite* the fact that we shall do our best to continually add newer topics and remove out-of-date ones. If we've missed one, please let us know in the comments, or submit a pull request to our [GitHub repo](https://github.com/Azure/azure-content/).

General Notes
-------------

The sections are broken down on the right of this page. (Links may occur in more than one section, as topics can be about more than one concept, distro, or technology.) In addition, there are several topics that describe various Linux options, image repositories, case studies, and how-to topics to upload your own custom images:

-	[Azure Marketplace](http://azure.microsoft.com/marketplace/virtual-machines/)

-	[MSOpenTech VM Depot](https://vmdepot.msopentech.com/List/Index)

-	[Events and Demonstrations: Microsoft Openness CEE](http://www.opennessatcee.com/)

-	[How to: Uploading your own Distro Image](https://azure.microsoft.com/documentation/virtual-machines-linux-create-upload-vhd) (and also instructions using an [Azure-Endorsed Distribution](https://azure.microsoft.com/documentation/virtual-machines-linux-endorsed-distributions)\)

-	[Notes: General Linux Requirements to Run in Azure](https://azure.microsoft.com/documentation/virtual-machines-linux-create-upload-vhd-generic)

-	[Notes: General Introduction for Linux on Azure](https://azure.microsoft.com/documentation/virtual-machines-linux-introduction)

<!--
- [Distros](#distros) &mdash; Topics to do with a specific distro.
- [The Basics](#basics) &mdash; A lot of the basic things to do that you either know or need to know.
- [Community Images and Repositories](#images) &mdash; Other places for very useful information, repositories, and binaries.
- [Languages and Platforms](#langsandplats)
- [Samples and Scripts](#samples)
- [Auth and Encryption](#security) &mdash; Important security-related topics, not necessarily specific to Azure.
- [Devops, Management, and Optimization](#devops) &mdash; A big category, changing rapidly.
- [Support, Troubleshooting, and "It Just Doesn't Work"](#supportdebug) &mdash; Really.
-->

Samples and Scripts
-------------------

Look for this section to fill up quickly. If you have suggestions, send us a PR or leave them in comments, below.

1.	[Create a multi-VM deployment using the Azure CLI](https://azure.microsoft.com/documentation/virtual-machines-create-multi-vm-deployment-xplat-cli)
2.	[Patrick Chanezon's Azure Linux GitHub repository](https://github.com/chanezon/azure-linux)
3.	[Video: How to Move On-Premises USB data on Linux to Azure using **usbip**](http://channel9.msdn.com/Blogs/Open/On-premises-USB-devices-on-Linux-on-Azure-via-usbip)
4.	[Video: Accessing Linux-based GUI on Azure in the Browser with fernapp](http://channel9.msdn.com/Blogs/Open/Accessing-Linux-based-GUI-on-Azure-over-browser-with-fernapp)
5.	[Video: Shared Storage on Linux Using Azure Files Preview -- Part 1](http://channel9.msdn.com/Blogs/Open/Shared-storage-on-Linux-via-Azure-Files-Preview-Part-1)
6.	[Video: Embracing Linux Devices on Azure using Service Bus and Web Sites](http://channel9.msdn.com/Blogs/Open/Embracing-Linux-devices-on-Azure-via-Service-Bus-and-Web-Sites)
7.	[Video: Connecting a Native Linux-based memcached application to Azure](http://channel9.msdn.com/Blogs/Open/Connecting-a-Linux-based-native-memcache-application-to-Windows-Azure)
8.	[Video: Load Balancing Highly Available Linux Services on Azure: OpenLDAP and MySQL](http://channel9.msdn.com/Blogs/Open/Load-balancing-highly-available-Linux-services-on-Windows-Azure-OpenLDAP-and-MySQL)

Data
----

This section contains information about several different storage approaches and technologies, including NoSQL, Relational, and Big Data.

### NoSQL

1.	[Blog: 8 Open-source NoSql Databases for Azure](http://openness.microsoft.com/blog/2014/11/03/open-source-nosql-databases-microsoft-azure/)
2.	Couchdb
	-	[Slideshare (MSOpenTech): Experiences with CouchDb on Azure](http://www.slideshare.net/brianbenz/experiences-using-couchdb-inside-microsofts-azure-team)
	-	[Blog: Running CouchDB-as-a-Service with node.js, CORS, and Grunt](http://msopentech.com/blog/2013/12/19/tutorial-building-multi-tier-windows-azure-web-application-use-cloudants-couchdb-service-node-js-cors-grunt-2/)
3.	MongoDB
	-	[How to: Create a Node.js Application on Azure with MongoDB using the MongoLab Add-On](https://azure.microsoft.com/documentation/store-mongolab-web-sites-nodejs-store-data-mongodb)
4.	Cassandra
	-	[How to: Running Cassandra with Linux on Azure and Accessing it from Node.js](https://azure.microsoft.com/documentation/virtual-machines-linux-nodejs-running-cassandra)
5.	Redis
	-	[Blog: Redis on Windows in the Azure Redis Cache Service](http://msopentech.com/blog/2014/05/12/redis-on-windows/)
	-	[Blog: Announcing ASP.NET Session State Provider for Redis Preview Release](http://blogs.msdn.com/b/webdev/archive/2014/05/12/announcing-asp-net-session-state-provider-for-redis-preview-release.aspx)
6.	RavenHQ
	-	[Blog: RavenHQ Now Available in the Azure Marketplace](http://azure.microsoft.com/blog/2014/08/12/ravenhq-now-available-in-the-azure-store/)

### Big Data

1.	Hadoop/Cloudera

	-	[Blog: Installing Hadoop on Azure Linux VMs](http://blogs.msdn.com/b/benjguin/archive/2013/04/05/how-to-install-hadoop-on-windows-azure-linux-virtual-machines.aspx)
	-	[How to: Get Started with Hadoop and Hive using HDInsight](https://azure.microsoft.com/documentation/hdinsight-get-started)  

2.	[Azure HDInsight](http://azure.microsoft.com/services/hdinsight/) -- a fully managed Hadoop service on Azure.

### Relational Database

1.	MySQL
	-	[How to: Install and Run MySQL](https://azure.microsoft.com/documentation/virtual-machines-linux-mysql-use-opensuse)
	-	[How to: Optimize Performance of MySQL on Azure](https://azure.microsoft.com/documentation/virtual-machines-linux-optimize-mysql-perf)
	-	[How to: MySQL Clusters](https://azure.microsoft.com/documentation/virtual-machines-linux-mysql-cluster)
	-	[How to: Create a MySQL Database using the Marketplace](https://azure.microsoft.com/documentation/store-php-create-mysql-database)
	-	[How to: Django and MySQL on Azure Websites with Python and Visual Studio](https://azure.microsoft.com/documentation/web-sites-python-ptvs-django-mysql)
	-	[How to: PHP and MySQL on Azure Websites with WebMatrix](https://azure.microsoft.com/documentation/web-sites-php-mysql-use-webmatrix)
	-	[MySQL High Availability Architecture in Microsoft Azure](http://download.microsoft.com/download/6/1/C/61C0E37C-F252-4B33-9557-42B90BA3E472/MySQL_HADR_solution_in_Azure.pdf)
2.	MariaDB
	-	[How to: Create a Multi-Master cluster of MariaDbs](https://azure.microsoft.com/documentation/virtual-machines-mariadb-cluster)
3.	PostgreSQL
	-	[How to: Install Ruby on Rails with Capistrano, Nginx, Unicorn, and PostgreSQL](https://azure.microsoft.com/documentation/virtual-machines-ruby-deploy-capistrano-host-nginx-unicorn)
4.	[Installing Postgres with corosync, pg_bouncer using ILB](https://github.com/chgeuer/postgres-azure)

Auth and Encryption
-------------------

Authentication and encryption are critical topics in software development, and there are many, many topics on the web that describe how to learn and use proper security techniques for both. We describe some of the basic usage to get up and running quickly with Linux and opensource workloads, as well pointing to tools to use to reset or remove remote security features on Azure. These are basic procedures, and we will be adding more complex scenarios soon.

1.	[The Basics: Certificate Use and Management](http://msdn.microsoft.com/library/azure/gg981929.aspx)
2.	[The Basics: SSH](https://azure.microsoft.com/documentation/virtual-machines-linux-use-ssh-key)
3.	[The Basics: How to Reset a Password or SSH Properties for Linux](https://azure.microsoft.com/documentation/virtual-machines-linux-use-vmaccess-reset-password-or-ssh)
4.	[The Basics: Using Root](https://azure.microsoft.com/documentation/virtual-machines-linux-use-root-privileges)

Devops, Management, and Optimization
------------------------------------

This section starts with a blog entry containing a series of videos on [Video: Azure Virtual Machines : Using Chef, Puppet and Docker for managing Linux VMs](http://azure.microsoft.com/blog/2014/12/15/azure-virtual-machines-using-chef-puppet-and-docker-for-managing-linux-vms/). However, the world of devops, management, and optimization is quite expansive and changing very quickly, so you should consider the list below a starting point.

1.	Docker

	-	[Docker VM Extension for Linux on Azure](https://azure.microsoft.com/documentation/virtual-machines-docker-vm-extension)
	-	[Using the Docker VM Extension from the Azure Command-line Interface (Azure CLI)](https://azure.microsoft.com/documentation/virtual-machines-docker-with-xplat-cli)
	-	[Using the Docker VM Extension from the Azure Preview Portal](https://azure.microsoft.com/documentation/virtual-machines-docker-with-portal)
	-	[Getting Started Quickly with Docker in the Azure Marketplace](https://azure.microsoft.com/documentation/virtual-machines-docker-ubuntu-quickstart)
	-	[How to use docker-machine on Azure](https://azure.microsoft.com/documentation/virtual-machines-docker-machine)
	-	[How to use docker with swarm on Azure](https://azure.microsoft.com/documentation/virtual-machines-docker-swarm)
	-	[Get Started with Docker and Compose on Azure](https://azure.microsoft.com/documentation/virtual-machines-docker-compose-quickstart)

2.	[Fleet with CoreOS](https://azure.microsoft.com/documentation/virtual-machines-linux-coreos-how-to)

3.	Deis

	-	[GitHub repo: Installing Deis on a CoreOS cluster on Azure](https://github.com/chanezon/azure-linux/tree/master/coreos/deis)

4.	Kubernetes

	-	[Complete guide to automated Kubernetes cluster deployment with CoreOS and Weave](https://github.com/GoogleCloudPlatform/kubernetes/blob/master/docs/getting-started-guides/coreos/azure/README.md#kubernetes-on-azure-with-coreos-and-weave)
	-	[Kubernetes Visualizer](http://azure.microsoft.com/blog/2014/08/28/hackathon-with-kubernetes-on-azure)

5.	Jenkins and Hudson

	-	[Blog: Jenkins Slave Plug-in for Azure](http://msopentech.com/blog/2014/09/23/announcing-jenkins-slave-plugin-azure/)
	-	[GitHub repo: Jenkins Storage Plug-in for Azure](https://github.com/jenkinsci/windows-azure-storage-plugin)
	-	[Third Party: Hudson Slave Plug-in for Azure](http://wiki.hudson-ci.org/display/HUDSON/Azure+Slave+Plugin)
	-	[Third Party: Hudson Storage Plug-in for Azure](https://github.com/hudson3-plugins/windows-azure-storage-plugin)

6.	Chef

	-	[Chef and Virtual Machines](https://azure.microsoft.com/documentation/virtual-machines-windows-install-chef-client)
	-	[Video: What is Chef and How does it Work?](https://msopentech.com/blog/2014/03/31/using-chef-to-manage-azure-resources/)

7.	Azure Automation

	-	[Video: How to Use Azure Automation with Linux VMs](http://channel9.msdn.com/Shows/Azure-Friday/Azure-Automation-104-managing-Linux-and-creating-Modules-with-Joe-Levy)

8.	Powershell DSC for Linux

	-	[Blog: How to do Powershell DSC for Linux](http://blogs.technet.com/b/privatecloud/archive/2014/05/19/powershell-dsc-for-linux-step-by-step.aspx)
	-	[GitHub: Docker Client DSC](https://github.com/anweiss/DockerClientDSC)

9.	[Ubuntu Juju](https://juju.ubuntu.com/docs/config-azure.html)

10.	[Packer plugin for Azure](https://github.com/msopentech/packer-azure)

Support, Troubleshooting, and "It Just Doesn't Work"
----------------------------------------------------

1.	Microsoft support documentation
	-	[Support: Support for Linux Images on Microsoft Azure](http://support2.microsoft.com/kb/2941892)

<!--Anchors-->

<!--Link references--In actual articles, you only need a single period before the slash. -->
