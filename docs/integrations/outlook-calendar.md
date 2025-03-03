---
sidebar_position: 2
---

# Outlook/Microsoft 365
The Outlook integration enables you to use your outlook.com or Microsoft 365 account to use for conflict checking and event bookings.

## Obtaining Microsoft Graph Client ID and Secret
1. Open [Azure App Registration](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps) and select New registration
2. Name your application
3. Set **Who can use this application or access this API?** to **Accounts in any organizational directory (Any Azure AD directory - Multitenant)**
4. Set the **Web** redirect URI to `<CALENDSO URL>/api/integrations/office365calendar/callback` replacing CALENDSO URL with the URI at which your application runs.
5. Use **Application (client) ID** as the **MS_GRAPH_CLIENT_ID** attribute value in .env
6. Click **Certificates & secrets** create a new client secret and use the value as the **MS_GRAPH_CLIENT_SECRET** attribute

## Removing Permissions for Cal to access your Microsoft Workplace Account

Hover over Cal in the My Apps portal, then select Manage your application

The top part of permissions window shows what you personally consented to. Examples of apps permissions include the ability to access your calendar, contacts, or camera.

You can revoke any of the permissions you consented to by selecting Revoke Permissions, however removing a permission may break some of the apps functionality. If you have problems after you remove permissions or accounts, contact your organization's Helpdesk for additional assistance.

If you require more help, head over the Microsoft Documentation Page about [Managing Applications](https://docs.microsoft.com/en-us/azure/active-directory/user-help/my-applications-portal-permissions-saved-accounts)
