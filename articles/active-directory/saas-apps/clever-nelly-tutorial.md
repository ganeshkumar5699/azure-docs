---
title: 'Tutorial: Azure AD SSO integration with Clever Nelly'
description: Learn how to configure single sign-on between Azure Active Directory and Clever Nelly.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: jeedes
---

# Tutorial: Azure AD SSO integration with Clever Nelly

In this tutorial, you'll learn how to integrate Clever Nelly with Azure Active Directory (Azure AD). When you integrate Clever Nelly with Azure AD, you can:

* Control in Azure AD who has access to Clever Nelly.
* Enable your users to be automatically signed-in to Clever Nelly with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Clever Nelly single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Clever Nelly supports **SP and IDP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add Clever Nelly from the gallery

To configure the integration of Clever Nelly into Azure AD, you need to add Clever Nelly from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Clever Nelly** in the search box.
1. Select **Clever Nelly** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for Clever Nelly

Configure and test Azure AD SSO with Clever Nelly using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Clever Nelly.

To configure and test Azure AD SSO with Clever Nelly, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Clever Nelly SSO](#configure-clever-nelly-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Clever Nelly test user](#create-clever-nelly-test-user)** - to have a counterpart of B.Simon in Clever Nelly that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Clever Nelly** application integration page, find the **Manage** section and select **Single sign-on**.
1. On the **Select a Single sign-on method** page, select **SAML**.
1. On the **Set up Single Sign-On with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type one of the following URLs:

    | Environment | URL Pattern |
    | - | - |
    | Test | `https://test.elephantsdontforget.com/plato`|
    | Production | `https://secure.elephantsdontforget.com/plato` |
    | | |

    b. In the **Reply URL** text box, type type one of the following URLs:

    | Environment | URL Pattern |
    | - | - |
    | Test | `https://test.elephantsdontforget.com/plato/callback?client_name=SAML2Client`|
    | Production | `https://secure.elephantsdontforget.com/plato/callback?client_name=SAML2Client` |
    | | |

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type one of the following URLs::

    | Environment | URL Pattern |
    | - | - |
    | Test | `https://test.elephantsdontforget.com/plato/sso/microsoft/index.xhtml`|
    | Production | `https://secure.elephantsdontforget.com/plato/sso/microsoft/index.xhtml` |
    | | |

1. On the **Set up Single Sign-On with SAML** page, In the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

	![The Certificate download link](common/copy-metadataurl.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Clever Nelly.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Clever Nelly**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you're expecting any role value in the SAML assertion, in the **Select Role** dialog, select the appropriate role for the user from the list and then click the **Select** button at the bottom of the screen.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Clever Nelly SSO

To configure single sign-on on **Clever Nelly** side, you need to send the **App Federation Metadata Url** to [Clever Nelly support team](mailto:support@elephantsdontforget.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Clever Nelly test user

In this section, you create a user called Britta Simon in Clever Nelly. Work with [Clever Nelly support team](mailto:support@elephantsdontforget.com) to add the users in the Clever Nelly platform. Users must be created and activated before you use single sign-on.

## Test SSO

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Clever Nelly Sign on URL where you can initiate the login flow.  

* Go to Clever Nelly Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Clever Nelly for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Clever Nelly tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Clever Nelly for which you set up the SSO. For more information, see [Azure AD My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Next steps

Once you configure Clever Nelly you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
