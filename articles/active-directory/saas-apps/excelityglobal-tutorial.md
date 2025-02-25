---
title: 'Tutorial: Azure AD SSO integration with
ExcelityGlobal'
description: Learn how to configure single sign-on between Azure Active Directory and ExcelityGlobal.
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
# Tutorial: Azure AD SSO integration with ExcelityGlobal

In this tutorial, you'll learn how to integrate ExcelityGlobal with Azure Active Directory (Azure AD). When you integrate ExcelityGlobal with Azure AD, you can:

* Control in Azure AD who has access to ExcelityGlobal.
* Enable your users to be automatically signed-in to ExcelityGlobal with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To configure Azure AD integration with ExcelityGlobal, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get a [free account](https://azure.microsoft.com/free/).
* ExcelityGlobal single sign-on enabled subscription.
* Along with Cloud Application Administrator, Application Administrator can also add or manage applications in Azure AD.
For more information, see [Azure built-in roles](../roles/permissions-reference.md).

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.

* ExcelityGlobal supports **IDP** initiated SSO.

> [!NOTE]
> Identifier of this application is a fixed string value so only one instance can be configured in one tenant.

## Add ExcelityGlobal from the gallery

To configure the integration of ExcelityGlobal into Azure AD, you need to add ExcelityGlobal from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **ExcelityGlobal** in the search box.
1. Select **ExcelityGlobal** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for ExcelityGlobal

Configure and test Azure AD SSO with ExcelityGlobal using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in ExcelityGlobal.

To configure and test Azure AD SSO with ExcelityGlobal, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure ExcelityGlobal SSO](#configure-excelityglobal-sso)** - to configure the single sign-on settings on application side.
    1. **[Create ExcelityGlobal test user](#create-excelityglobal-test-user)** - to have a counterpart of B.Simon in ExcelityGlobal that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **ExcelityGlobal** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows to edit Basic S A M L Configuration.](common/edit-urls.png "Basic Configuration")

4. On the **Basic SAML Configuration** page, perform the following steps:

    a. In the **Identifier** text box, type one of the
     following URLs:

    | **Identifier** |
    |------|
    | **For Production Environment** : `https://ess.excelityglobal.com` |
    | **For Sandbox Environment** : `https://s6.excelityglobal.com` |

    b. In the **Reply URL** text box, type one of the following URLs:

    | **Reply URL** |
    |----------|
    | **For Production Environment** : `https://ess.excelityglobal.com/ACS` |
    |**For Sandbox Environment** : `https://s6.excelityglobal.com/ACS` |

1. Your ExcelityGlobal application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes, whereas **nameidentifier** is mapped with **user.userprincipalname**. ExcelityGlobal application expects **nameidentifier** to be mapped with **user.mail**, so you need to edit the attribute mapping by clicking on **Edit** icon and change the attribute mapping.
 
	![Screenshot shows the image of ExcelityGlobal application.](common/edit-attribute.png "Image")

1. In the **SAML Signing Certificate** section, click **Edit** button to open **SAML Signing Certificate** dialog.

	![Screenshot shows to edit SAML Signing Certificate.](common/edit-certificate.png "Certificate")

1. In the **SAML Signing Certificate** section, copy the **Thumbprint** and save it on your computer.

    ![Screenshot shows to Copy Thumbprint value.](common/copy-thumbprint.png "Thumbprint")

1. On the **Set up ExcelityGlobal** section, copy the appropriate URL(s) as per your requirement.

	![Screenshot shows to copy configuration appropriate U R L.](common/copy-configuration-urls.png "Metadata")

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

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to ExcelityGlobal.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **ExcelityGlobal**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you're expecting any role value in the SAML assertion, in the **Select Role** dialog, select the appropriate role for the user from the list and then click the **Select** button at the bottom of the screen.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure ExcelityGlobal SSO

To configure single sign-on on **ExcelityGlobal** side, you need to send the **Thumbprint value** and appropriate copied URLs from Azure portal to [ExcelityGlobal support team](https://www.excelityglobal.com/contact-us). They set this setting to have the SAML SSO connection set properly on both sides.

### Create ExcelityGlobal test user

In this section, you create a user called Britta Simon in ExcelityGlobal. Work with [ExcelityGlobal support team](https://www.excelityglobal.com/contact-us) to add the users in the ExcelityGlobal platform. Users must be created and activated before you use single sign-on.

## Test SSO

In this section, you test your Azure AD single sign-on configuration with following options.

* Click on Test this application in Azure portal and you should be automatically signed in to the ExcelityGlobal for which you set up the SSO.

* You can use Microsoft My Apps. When you click the ExcelityGlobal tile in the My Apps, you should be automatically signed in to the ExcelityGlobal for which you set up the SSO. For more information, see [Azure AD My Apps](/azure/active-directory/manage-apps/end-user-experiences#azure-ad-my-apps).

## Next steps

Once you configure ExcelityGlobal you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).