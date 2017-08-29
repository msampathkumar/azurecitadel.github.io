---
layout: article
title: Azure 101 Content
date: 2017-07-04
categories: null
permalink: /azure101/portal/
tags: [azure, 101, lab, portal, network, resource, group, vNet]
comments: true
author: Richard_Cheney`
image:
  feature: 
  teaser: Education.jpg
  thumb: 
---
Introductory portal lab for the Azure 101 workshop. 

{% include toc.html %}

# Azure 101 Portal Lab

## Accessing the Azure Portal

The main Azure portal is <https://portal.azure.com>.

Login using the account for your Azure subscription. Your account
information is at the top right, including password change, and viewing
permissions and your bill.  Next to that is the Help + Support, for accessing the help or opening up
a support ticket. 

Click on the Help + Support icon and then:
-   launch the guided tour
-   see what’s new
-   check the keyboard shortcuts

Clicking on the cog icon shows the Portal Settings. You can filter
multiple subscriptions, change the language and certain portal
characteristics.
-   Change the theme

Next to the Azure Cloud Shell is the _Notifications_ section, for status
updates, billing updates and to show deployment activity.

## Dashboard Customisation

The Azure portal enables you to have multiple dashboards and to
customise those dashboards. You can also share dashboards with other AAD
users or groups within the subscription, leveraging the role based
access control (RBAC) to control who has access.

-   Create a new dashboard, and name it "Azure 101".
-   From the Tile Gallery’s General area, pull across the following items:
    -   All Resources Reconfigure (using the ellipsis (…)) to change to
        4x4 tiles
    -   Clock Reconfigure to 2x1, 24 hour, and London time
    -   Quickstart Tutorials
    -   Markdown change title to "Azure 101", subtitle to Useful Links,
        and replace the content with the markdown shown below and then resize
        to fit.

Open this [Markdown file](./portalMarkdown.txt) and copy the contents.

```
### Documentation

* [Products](https://azure.microsoft.com/en-us/services) and [Pricing]( https://azure.microsoft.com/en-us/pricing/)
* [Azure Docs](https://docs.microsoft.com/en-us/azure/) and [Subscription Limits](https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits)
* [Architecture](https://docs.microsoft.com/en-us/azure/index#pivot=architecture)
* [Learning Paths](https://azure.microsoft.com/en-us/documentation/learning-paths/)
* Interactive [Azure Services](http://azureplatform.azurewebsites.net/en-us/) Overview
* Azure [Resource Explorer](https://resources.azure.com/) and [Storage Explorer](http://storageexplorer.com/)
* Azure [Price Calculator](https://azure.microsoft.com/en-us/pricing/calculator/) and [TCO Calculator](https://www.tco.microsoft.com/)


### Partner Portals

* [MPN Portal](http://partner.microsoft.com/)
* [Cloud Solution Partner (CSP)](https://partner.microsoft.com/en-us/cloud-solution-provider)
* [Azure Account Portal](http://account.windowsazure.com/Subscriptions)
* [Partner Support](https://partner.microsoft.com/en-GB/support), including [Advanced Support for Partners (ASP)](https://partner.microsoft.com/en-US/Support/advanced-cloud-support?advancedcloudsupport) and [Visual Studio Subscriptions](https://support.microsoft.com/kb/4013871/?tpqid=800-000036) 
* [Cloud Practice Playbooks](https://partner.microsoft.com/en-US/campaigns/cloud-practice-playbooks) and [Partner Concierge](https://aka.ms/ukconcierge) for marketing

### Training Resources

* [OpenEdx MOOC Courses](https://openedx.microsoft.com/)
* [Channel9](https://channel9.msdn.com/)
* [Microsoft Virtual Academy](https://mva.microsoft.com/product-training/microsoft-azure)
* [Partner University](https://partner.microsoft.com/en-gb/training), including [Partner Upskill](https://aka.ms/mpnukupskill) and [Cloud and Proud](https://www.microsoft.com/uk/partner/cloudandproud/)
* Prep guides for [70-533](https://mva.microsoft.com/en-US/training-courses/certification-exam-overview-70-533-implementing-microsoft-azure-infrastructure-solutions-17405) and [70-534](https://mva.microsoft.com/en-us/training-courses/certification-exam-overview-70-534-architecting-microsoft-azure-solutions-17406)

### Keeping Up To Date

* [Azure Blog](https://azure.microsoft.com/en-gb/blog/)
* [Azure Weekly](https://buildazure.com/)
* Azure Public Preview [Roadmap](https://www.microsoft.com/en-us/cloud-platform/roadmap-public-preview)
* [Roadmap](https://azure.microsoft.com/en-gb/roadmap/) and [Updates]( https://azure.microsoft.com/en-gb/updates/)
* Azure [Preview Portal](http://preview.portal.azure.com)
```

Once complete, your dashboard should look something like this:

![](../../images/Az101-Dashboard.jpg)

## Documentation

Let’s click through some of the documentation links in the Markdown box:

-   Interactive [Azure
    Services](http://azureplatform.azurewebsites.net/en-us/) Overview
-   [Products](https://azure.microsoft.com/en-us/services) and [Pricing](https://azure.microsoft.com/en-us/pricing)
-   [Azure Docs](https://docs.microsoft.com/en-us/azure)
-   [Architecture](https://docs.microsoft.com/en-us/azure/index#pivot=architecture)
-   [Learning
    Paths](https://azure.microsoft.com/en-us/documentation/learning-paths)


------------------------------------------------------------------

## Create a resource group called Azure101IaaS

-   Open the Azure [portal](http://portal.azure.com)
-   Choose one of the following options:
    -   Click on the + New icon (or G+N), search for _Resource Group_ and click on it.
    -   Click on _Resource Groups_ in your favourites and click on **Add**
    -   Click on the _More Services_ icon, _Resource Groups_ in the General section and then on **Add**
-   Create the resource group using the following values:
    -   Resource Group Name: _Azure101IaaS_
    -   Resource Group Location: _West Europe_
-   Note the deployment notification area
-   Refresh the resource groups and click on the _Azure101IaaS_ resource group

## Create a Virtual Network (VNet) with two subnets

-   Add a Virtual Network:
    -   Click on the **+**
    -   Search on _Virtual Network_
    -   Select, then Create
-   **Name:** _azure101vNet_
-   **Address space:** _10.4.0.0/16_
-   **Subnet name:** _webSubnet_
-   **Subnet address range:** _10.4.1.0/24_

Once created, click into the VNet and add the second subnet:
-   Select subnets on the blade
-   Add _dbSubnet_ (10.4.2.0/24)

If you have completed the lab early then search on information in the portal and on the Azure docs area for:
-   Network Security Groups (NSGs)
-   GatewaySubnet
-   ExpressRoute and Site-to-Site (S2S) VPN Gateways
-   Network Virtual Appliances
-   User Defined Routes (UDRs) in Route Tables
-   vNet Peering
-   Region to region S2S VPNs