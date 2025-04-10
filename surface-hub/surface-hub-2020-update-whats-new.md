---
title: What's new in Windows 10 Team 2020 updates for Surface Hub and Surface Hub 2S
description: Learn about new features and improvements in Windows 10 Team 2020 updates for Surface Hub and Surface Hub 2S, including manageability and security.
ms.service: surface-hub
author: coveminer
ms.author: chauncel
manager: frankbu
ms.topic: overview
ms.date: 10/28/2024
ms.localizationpriority: Medium
appliesto:
- Surface Hub
- Surface Hub 2S
---

# What's new in Windows 10 Team 2020 updates for Surface Hub and Surface Hub 2S

Surface Hub receives periodic updates to enhance features and functionality. The 2020 Update (20H2), including Update 1 and Update 2, delivers key improvements to device deployment and manageability.

> [!NOTE]
> This update applies only to Surface Hub (1st generation) and Surface Hub 2S.  

## Windows 10 Team 2020 Update 2

[!INCLUDE [Hub 2S EoS](includes/hub2s-eos.md)]

### Display and preferred language support

Admins can now enable end users to [change the display language](change-language-on-surface-hub.md) from installed languages on the device. Ensure that Surface Hub is running [KB5023773](https://support.microsoft.com/help/5023773) or a later Windows update. For more details, visit the [Surface Hub update history](surface-hub-update-history.md).  

### GCC High support

With [KB5010415](https://support.microsoft.com/help/5010415) or later installed, Surface Hub supports Government Community Cloud (GCC) High environments. [More configuration steps](surface-hub-teams-rooms.md#support-for-teams-rooms-in-government-community-cloud-high-gcc-h) are required for Teams Rooms to connect to GCC High tenants successfully.  

### Support for Surface Hub Smart Camera

The AI-powered Surface Hub Smart Camera enhances hybrid collaboration, ensuring remote participants see interactions with both content and in-room participants. Learn more about installation at [Install and manage Surface Hub Smart Camera](surface-hub-smart-camera.md).  

### Support for Progressive Web Apps (PWAs)

Admins can deploy PWAs remotely on Surface Hubs via an MDM provider using provisioning packs. For more information, see [Install Progressive Web Apps on Surface Hub](install-pwa-surface-hub.md).  

### Ease of Access updates

Users can adjust Ease of Access settings during a Surface Hub session and close apps just like they do in other versions of Windows 10 or Windows 11.

- **Ease of Access**. Users can adjust the following settings without signing in:   Display, Text cursor, Magnifier, High contrast, Narrator, Closed captions, and Keyboard.
- **Familiar UI for apps**. Users can close apps using the familiar **Close** button, reducing dependency on dragging apps to the bottom of the screen.  

More details are available at [Adjust Ease of Access settings on Surface Hub](accessibility-surface-hub.md).  

### Administrator updates

- **Event Viewer access:** Now accessible from the Settings app.  
- **New MDM policies:** Updates include the following Configuration service providers (CSPs):  
  - [TimeLanguageSettings-CSP](/windows/client-management/mdm/policy-csp-timelanguagesettings)  
  - [LocalUsersAndGroups-CSP](/windows/client-management/mdm/policy-csp-localusersandgroups)  

See [Configure non-Global Admin accounts on Surface Hub](surface-hub-2s-nonglobal-admin.md) for further admin configurations.  

## Windows 10 Team 2020 Update 1

### Support for new Teams Rooms application

### New Teams Rooms client support  

With [KB5005101](https://support.microsoft.com/help/5005101) or later, Surface Hubs automatically upgrade to the latest [Teams Rooms client](surface-hub-teams-rooms.md).  

### Whiteboard application upgrade  

This update facilitates the transition to the new [Whiteboard app](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/unified-whiteboard-experience-coming-to-surface-hub/ba-p/3145226) via Microsoft Store.  

### New Microsoft Edge browser installed by default

After installation of this update, Surface Hubs automatically replace their Microsoft Edge Legacy browser with the new Chromium-based browser. To learn more, see [Manage Microsoft Edge on Surface Hub](surface-hub-install-chromium-edge.md). Microsoft Edge Legacy is no longer available on Windows 10 Team after installation of this update or a subsequent Windows Cumulative Update (CU).

## Windows 10 Team 2020 Update (20H2)

### Deployment and manageability

- **Modern authentication for cloud device accounts**. Surface Hub supports Exchange Web Services (EWS) and Microsoft Authentication Library-based authentication to connect to Exchange, allowing customers to deprecate the use of Basic authentication. To learn more, see [Modern authentication on Surface Hub](surface-hub-modern-auth.md).
- Expanded Mobile Device Management (MDM) policy settings:** Over 20 new policies enhance control over updates, wireless projection, network configuration, and privacy settings. Key CSPs include:  

  - [Accounts CSP](/windows/client-management/mdm/accounts-csp)
  - [Firewall-CSP](/windows/client-management/mdm/firewall-csp)
  - [RemoteWipe CSP](/windows/client-management/mdm/remotewipe-csp)
  - [Wifi-CSP](/windows/client-management/mdm/wifi-csp)
  - [Wirednetwork-CSP](/windows/client-management/mdm/wirednetwork-csp)

To learn more, see the following resources:

- [CSPs supported in Microsoft Surface Hub](/windows/client-management/mdm/configuration-service-provider-reference#surfacehubcspsupport)
- [Manage Surface Hub with an MDM provider](manage-settings-with-mdm-for-surface-hub.md)

<a name='azure-active-directory-joined-devices'></a>

---

### Microsoft Entra joined devices

- **Single sign-on (SSO):** Credentials flow seamlessly across Microsoft 365 apps on Microsoft Entra joined devices.  
- **Conditional access (CA):** Enforce policies for Microsoft Entra joined Surface Hubs per corporate security requirements.  
- **Non-Global admin support:** Assign admins with specific permissions to manage Surface Hub.  To learn more, see [Configure non-Global Admin accounts on Surface Hub](surface-hub-2s-nonglobal-admin.md).

> [!IMPORTANT]
> Microsoft recommends that you use roles with the fewest permissions. This helps improve security for your organization. Global Administrator is a highly privileged role that should be limited to emergency scenarios when you can't use an existing role. To learn more, see the recommended guidance in [Configure non-Global Admin accounts on Surface Hub](surface-hub-2s-nonglobal-admin.md).

---

## Inking improvements  

- **Dual-pen support:** Collaborate on Surface Hub 2S with two pens for real-time interaction. Ensure the latest firmware updates are installed.  

### Microsoft Teams  

- **Microsoft Teams installed by default**. Microsoft Teams is the default app for meetings, calls, and collaboration on new Surface Hub devices, which can be changed or configured via MDM or directly on Surface Hub using the Settings app. To learn more, see [Deploy Microsoft Teams](/MicrosoftTeams/teams-surface-hub).
- **Proximity Join:**   Proximity Join lets users take scheduled Microsoft Teams calls on a nearby Surface Hub using their laptop or phone. It also lets users transition an in-progress meeting to a nearby Surface Hub. Windows 10 Team 2020 Update adds Mobile Device Management (MDM) support to configure Proximity Join. To learn more, see:

  - [Microsoft Teams Blog](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/microsoft-teams-devices-for-shared-spaces-july-and-august-update/ba-p/1604833).
  - [Manage Microsoft Teams settings on Surface Hub](/MicrosoftTeams/rooms/surface-hub-manage-config)

- **Coordinated Meetings:** Utilize multiple devices for Teams meetings, maximizing screen use with separate content and video feeds.  Users can join a meeting from another device with a single tap and maximize screen real estate by showing video feeds on one device and a digital whiteboard or content on the other. Windows 10 Team 2020 Update adds MDM support to configure Coordinated Meetings. To learn more, see [Set up Coordinated Meetings with Microsoft Teams Rooms and Surface Hub](/MicrosoftTeams/rooms/coordinated-meetings).

### Security

- **Passwordless sign-in:** Users can sign in quickly with FIDO2 security keys or Microsoft Authenticator for seamless access to meetings and resources. To learn more, see [Configure passwordless sign-in on Surface Hub](surface-hub-2s-phone-authenticate.md).
**Microsoft Entra ID improvements:** Users can now authenticate with email aliases or UPNs through Microsoft Authenticator. To learn more, see [Sign in to Surface Hub with Microsoft Authenticator](surface-hub-authenticator-app.md).

## Learn more

- [Surface Hub update history](surface-hub-update-history.md).
- [Windows 10 Team 2020 Update 1 released to all Surface Hubs](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/windows-10-team-2020-update-1-released-to-all-surface-hubs/ba-p/2653503)
- [Windows 10 Team 2020 Update available October 27](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/surface-hub-windows-10-team-2020-update-available-october-27/ba-p/1810739)
