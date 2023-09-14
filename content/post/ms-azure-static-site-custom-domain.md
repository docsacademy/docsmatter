+++
author = "Vladimir Likhanov"
title = "Microsoft Azure - configuring a custom domain"
date = "2022-12-09"
description = "Microsoft Azure"
featured = true
draft = true
tags = [
    "Azure"
]
categories = [
    "Static website",
    "Custom domain"
]
thumbnail = "images/blog/azure/azure-logo.png"
+++

> In this post, you'll know how to configure your Azure endpoint for use with a custom domain.

If you are interested in how to set up Microsoft Azure to host your static website, see [Microsoft Azure - hosting a static website]
(/post/ms-azure-static-site-setup.md).

To set up a custom domain for use with an endpoint in Microsoft Azure, you need to create a CNAME record with your DNS provider.
This recourd must point to your endpoint. The procecure slightly differs depending on your DNS provider.

but you need to first add a CNAME that points to the address of the static website generated by the Blob Storage through your DNS provider. Once this CNAME is created, go to the Azure portal, on the Storage Account and find the option "Custom Domain". From there you can add the domain name in such a way that the Storage Account allows connections from this domain name.

You can configure a custom domain with a static website by using Azure Content Delivery Network (Azure CDN). Azure CDN provides consistent low latencies to your website from anywhere in the world.

Azure Content Delivery Network offers a global solution for rapidly delivering content.

These are steps you'll need to complete:

* Creating a CDN profile
* Adding a custom domain to Azure
* Creating a CNAME record with your DNS provider

## Creating a CDN profile

First, you need to create a CDN profile:

1. Go to the **Home** page of your Azure account.

2. Enter **CDN** in the **Search** field.

* The **Front Door and CDN profiles** entry is displayed as one of the offered search results.

![Microsoft Azure - searching for CDN profiles](/images/blog/azure/azure-searching-for-cdn-profiles.png)

3. Click on the **Front Door and CDN profiles** entry.

* The **Front Door and CDN profiles** page opens.

![Microsoft Azure - existing CDN profiles](/images/blog/azure/azure-cdn-profiles-page.png)

4. Click on the **+ Create** button.

* The **Compare offerings** page opens where you can choose the desired Front Door offering.

![Microsoft Azure - choosing a Front Door offering](/images/blog/azure/azure-cdn-profiles-compare-offerings.png)

5. Accept the default choices by clicking on the **Continue to create a Front Door** button at the bottom of the page.

* The **Create a Front Door profile** page opens.

6. Fill out the following fields:

**Project details**

* **Subscription**: Choose your Azure subscription. This must be the same subscription as used for your static website.
* **Resource group**: Choose the resource group. This must be the same group as used for your static website.
* **Resource group location**: This field is not editable and filled out automatically on the basis of the chosen
resource group.

![Microsoft Azure - Front Door - filling out project details](/images/blog/azure/azure-front-door-project-details.png)

**Profile details**

* **Name**: Enter a name for your CDN profile.
* **Tier**: Make sure that the **Standard** option is selected.

![Microsoft Azure - Front Door - filling out profile details](/images/blog/azure/azure-front-door-profile-details.png)

**Endpoint settings**

* **Endpoint name**: Unique name for your endpoint. Expand info!
* **Origin type**: Choose **Storage (Static website)**. Check if all have this!
* **Origing host name**: Choose the hostname of your static website.

![Microsoft Azure - Front Door - filling out endpoint settings](/images/blog/azure/azure-front-door-endpoint-settings.png)

7. Click on the **Review + Create** button at the bottom of the page.

8. Review your settings and click on the **Create** button.

* Your CDN profile is created.
* Now your static website is also available at the endpoint you entered in the **Endpoint name** field under **Endpoint settings**
(see the exact name in the **Endpoint hostname** field).

## Configuring a custom domain

1. Open the **Front Door and CDN profiles** page.

2. Click on your profile name.

* The configuration page for your profile opens.

3. On the **Overview** tab, navigate to the **Properties** section, and click on **Custom domains**.

![Microsoft Azure - creating a custom domain](/images/blog/azure/Azure-creating-custom-domain.png)