---
title: First party license management enabled in Microsoft Teams
description: Learn how to enable customers to easily assign, use, and track SaaS licenses purchased in Teams storefront.
author: v-dreddipogu
ms.author: surbhigupta
ms.topic: how-to
ms.localizationpriority: high
---

# First party license management enabled in Teams for third-party SaaS offers

The Microsoft Teams Third-party app license management provides the flexibility for customers to assign, use, and track SaaS licenses purchased from Team Storefront. This article details on the critical task of license management – the ability to authorize specific users to use a particular ISV application for the paid duration. With first party license management of third party SaaS offers in the Teams surface area, the license management happens post-purchase of the said app (the associated SaaS offer) via Teams surface areas or AppSource. The app is unusable if the licenses aren't assigned.

Third-party app license management enables independent software vendors (ISVs) to manage and enforce licenses for their solutions using systems provided by Microsoft. By adopting this, ISVs can:

* Enable customers to assign and unassign licenses of ISV products using Teams and Teams Admin Center.
* Lessen the effort of building and maintaining their own license management and enforcement system.
* Elaborate how Teams will connect the apps with license management.

## Impacts on ISVs

The ISV creates an offer in Partner Center and manage licenses for this offer through Microsoft. This includes defining one or more licensing plans for the offer.  

* ISV needs to ensure the mapping of offers that have licenses managed by Microsoft.
* When a user within the customer’s organization tries to run an application, license usage rights check is done by the ISV with Microsoft Graph to ensure that user has an active license.
* ISVs can view information on provisioned and assigned licenses over time and by geography in Partner Center.

## Pre-requisites

Following are the pre-requisites for enabling third-party app license management in Dynamics 365 customer engagement and Power Apps.

* Valid partner (MPN) account at Microsoft.  
[Create an MPN account in Partner Center - Partner Center | Microsoft Docs](/partner-center/mpn-create-a-partner-center-account)
* Enrollment in commercial marketplace program.
[Introduction to the Microsoft commercial marketplace - Learn | Microsoft Docs](/learn/modules/intro-commercial-marketplace/)
* [Create a commercial marketplace account in Partner Center for Azure Marketplace | Microsoft Docs](/azure/marketplace/create-account)

* Access to development environments and tools required to create Teams Add-ons.

* A test tenant with a Teams environment in it. This is to simulate how a customer will experience the license management or enforcement for your solution.  

## Chapter 1: Defining an offer in Partner Center

1. Create an offer in Partner Center.
1. Define the licensing options.
1. Add one or more plans.
1. Copy service IDs from offer details and update your Teams app to map to the paid functionality.
1. Map your Teams app to your offer and publish.
1. Best practices on ISV logic to determine ISV managed offers vs Microsoft managed offers for license management.

### Create an offer in Partner Center

1. Log in to [Partner Center](https://partner.microsoft.com/) and click on “Partner Center” to open your dashboard.

    :::image type="content" source="~/assets/images/first-party-license-mgt/partner-center-home-page.png" alt-text="Partner Center Homepage":::

1. Select **Commercial Marketplace** or **Overview** on left pane and then select **New Offer**. Now select **Software as a Service** to create a new offer.

    :::image type="content" source="~/assets/images/first-party-license-mgt/commercial-marketplace.png" alt-text="Commercial marketplace":::

1. To create an offer, enter **Offer ID** and **Offer alias** and select **Create**.

    > [!NOTE]
    > If you're creating an offer for testing purpose, add the text **-ISVPILOT** to the end of your offer alias. This indicates the certification team that the offer is for testing purposes. Microsoft delete offers with **-ISVPILOT** periodically. So, don't use this tag for reasons other than testing the license management capability.

(Image)

### Define the licensing options

To enable license management for your offer, select the checkbox (Placeholder).

> [!NOTE]
> This is a one-time setting, and you cannot change it once your offer is published.

(Image)

### Add one or more plans

1. Select **Plan overview** on left pane and then select **Create new plan** to define the plans you want to enable for the offer. You're required to define *at least* one plan.

(Image)

1. Select **Create** and enter your plan description in the page. Now select **Save draft** to save the plan information. This plan information displays on Teams marketplace and [Appsource](https://appsource.microsoft.com/) under offer listing (plans section).

(Image)

1. Add pricing and availability details (placeholder).

(Image)

1. Select **Plan overview** to go to the listing page that shows all the plans you've created for this offer.

(Image)

### Copy service IDs from offer details and update your Teams app to map to the paid functionality

(Content and image needs to be added)

### Map your Teams app to your offer and publish

(content and image needs to be added)

### Best practice on ISV logic

(Content and image needs to be added)

## Chapter 2: Offer availability in Teams and Appsource

(Need content)

## Chapter 3: Purchase offer in Teams or Appsource

1. In Teams, go to the Appstore and select your app.
1. Select **Buy a subscription**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/buy-subscription.png" alt-text="Buy subscription":::

1. Select the plan you want to purchase and select **Checkout**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/checkout-button.png" alt-text="Checkout button":::

1. Enter the number of licenses you would like to purchase, update sold to address and payment information. Select “place order”. This completes the purchase of the subscription.

    :::image type="content" source="~/assets/images/first-party-license-mgt/place-order.png" alt-text="Place order":::

1. Once subscription is purchased successfully, purchaser is redirected to the ISV site to complete configuration steps required to activate the subscription.

    :::image type="content" source="~/assets/images/first-party-license-mgt/configure-now.png" alt-text="Configure button":::

## Chapter 4: Manage third-party licenses in Teams

1. On Teams client, subscription purchaser can manage license assignments from within the Teams. From **Manage your apps**, you can go to **Subscriptions** tab to view the list of purchases.

    :::image type="content" source="~/assets/images/first-party-license-mgt/manage-your-apps.png" alt-text="Manage your apps":::

1. On the **Subscriptions** tab, select **Assign licenses** to manage licenses for the purchases.

    :::image type="content" source="~/assets/images/first-party-license-mgt/manage-your-apps-page.png" alt-text="Manage your apps page":::

1. Purchaser is able to view license utilization and assign licenses by selecting **Assign licenses**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/assign-licenses-button.png" alt-text="Assign licenses button":::

1. Purchaser can begin assigning licenses to users in the tenant by entering the user names. Purchaser can add one or more users for license assignment.

    :::image type="content" source="~/assets/images/first-party-license-mgt/assign-licenses-popup.png" alt-text="Assign licenses popup":::

1. Select **Assign** after adding all the users.

    :::image type="content" source="~/assets/images/first-party-license-mgt/assign-button.png" alt-text="Assign button":::

1. Licenses are successfully assigned and purchaser sees the list of assigned users as below.

    :::image type="content" source="~/assets/images/first-party-license-mgt/users-assigned-successfully.png" alt-text="Users were assigned licenses":::

1. Purchaser can also assign licenses to a **Team** in Teams. Purchaser can search for the team and select **Assign**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/assign-licenses-to-team.png" alt-text="Assign licenses to team":::

1. If the number of users in the team exceeds the number of available licenses, the purchaser can select a subset of users to whom licenses are assigned. After doing so, select **Save**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/save-button.png" alt-text="Save button":::

1. Purchaser can unassign licenses from one or multiple users from the license page. The purchaser can select the users and select **Unassign**.

    :::image type="content" source="~/assets/images/first-party-license-mgt/unassign-button.png" alt-text="Unassign button":::

1. If there is a delay in a multi user assignment or un-assignment action, the purchaser sees a **Pending** status while the action completes on the Microsoft services.

    :::image type="content" source="~/assets/images/first-party-license-mgt/pending-status.png" alt-text="Pending status":::

## Chapter 5: Test the app by launching in Teams environment

### App runtime consent flow for user

(Content)

## Check license usage in Partner Center analytics

### Check license usage of ISV apps in the Partner Center analytics section

1. Sign into [Partner Center](https://partner.microsoft.com/) with your partner account.
1. In the left pane, select **Commercial Marketplace > Analyze > Licensing** to go to licensing dashboard.
1. Select the **Plan** and **Tenant** in the reporting widget to see the month wise usage.

(Image)

## Limitations

APIs are managed by commerce team for license management. If a user is assigned with a license, in the background you're sending an API request to license core on commerce to add a license.

If a license is assigned to multiple users, you build a queue to the commerce team to add the licenses.

* Partial failures - A user may or may not have approval, or their matrix may be a failure in the API assignment action, so there could be a partial failure in assigning licenses.

* Time lag based on the queue - There may be a lag based on number of users in the queue that needs to be assigned.

You'll see a pending status if the license has failed to assign and there is an opportunity to **Retry**.