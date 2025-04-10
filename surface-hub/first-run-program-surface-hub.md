---
title: First-time setup for Surface Hub
description: Set up Surface Hub for the first time with guided steps, account options, and provisioning support for a consistent experience.
ms.assetid: 07C9E84C-1245-4511-B3B3-75939AD57C49
ms.reviewer: 
manager: frankbu
ms.service: surface-hub
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.date: 03/31/2025
ms.localizationpriority: medium
appliesto:
- Surface Hub 
- Surface Hub 2S
---

# First-time setup for Surface Hub

[!INCLUDE [Hub 2S EoS](includes/hub2s-eos.md)]

When you first start Surface Hub, the device automatically enters first-time setup mode to guide you through account configuration and related settings.

For Surface Hub 3, see [First-time setup for Surface Hub running Microsoft Teams Rooms on Windows](first-run-program-surface-hub-3.md). 

> [!TIP]
> As a companion to this article, we recommend using the [Surface Hub and Microsoft Teams Rooms automated setup guide](https://go.microsoft.com/fwlink/?linkid=2221605) when signed in to the Microsoft 365 Admin Center. This guide customizes your experience based on your environment. If you're hosted in Exchange Online and using Microsoft Teams, the guide will automatically create your device account with the correct settings. Or use it to validate existing resource accounts to help turn them into compatible Surface Hub device accounts. To review best practices without signing in and activating automated setup features, go to the [Microsoft 365 Setup portal](https://go.microsoft.com/fwlink/?linkid=2222648). 

> [!NOTE]
> You can automate the setup process with a [Provisioning package](#use-provisioning-packages) to ensure a consistent experience across multiple Surface Hubs.

## Get started

1. By default, Cortana is enabled to guide you through the process. To turn off Cortana assistance, select the microphone icon.

    :::image type="content" source="images/hub-setup-cortana.png" alt-text="Cortana is enabled to guide you through the process.":::

2. **Select your region**. Confirm the autodetected region and select **Yes**.

    :::image type="content" source="images/hub-setup-region.png" alt-text="Select your region.":::

3. **Confirm keyboard layout**. Select **Yes**.

    :::image type="content" source="images/hub-setup-keyboard.png" alt-text="Confirm keyboard layout.":::

4. To add a second keyboard, select **Add layout**. Otherwise, select **Skip**.

    :::image type="content" source="images/hub-setup-2keyboard.png" alt-text="Add a second keyboard.":::

5. **Connect to a network**. If you have already attached an Ethernet cable, Surface Hub automatically connects to your network. Alternatively, you can connect to a wireless network. **Note:** You can't connect to a wireless network in hotspots (captive portals) that redirect sign-in requests to a provider's website. Select **Next**.

    :::image type="content" source="images/hub-setup-network.png" alt-text="Connect to a network.":::

6. **Accept Windows 10 License Agreement**. Select **Accept**.

    :::image type="content" source="images/hub-setup-license.png" alt-text="Accept Windows 10 License Agreement.":::

7. **Enter Device account info** using a UPN address (user@contoso.com) or a down-level domain address (CONTOSO\user). Use the format that matches your environment and enter the password.

    :::image type="content" source="images/hub-setup-device-account.png" alt-text="Enter Device account info.":::

  | Environment                                              | Required format for device account |
  | -------------------------------------------------------- | ---------------------------------- |
  | Device account is hosted only online                     | username@contoso.com               |
  | Device account is hosted only on-premises                | CONTOSO\user                       |
  | Device account is hosted online and on-premises (hybrid) | CONTOSO\user                       |

  > [!NOTE]
  > You can skip device account setup, but the device won't be fully integrated into your infrastructure. If skipped, you can add a device account later in the Settings app.

8. **Enter your password** and select **Next**.

9. Surface Hub automatically detects Exchange server and SIP address information from the domain entered in the previous step. Or, if needed, provide your Exchange server address and select **Next**.

    :::image type="content" source="images/hub-setup-exchange.png" alt-text="Exchange server and SIP address.":::

10. **Name this device**. Enter a name for your device or use the suggested one. **Select Next**.

    :::image type="content" source="images/hub-setup-name.png" alt-text="Name this device.":::

   - The **Friendly name** is visible on the bottom left corner of Surface Hub 2S and is shown when projecting to the device.
   - The **Device name** identifies the device when affiliated with Active Directory or Microsoft Entra ID and when enrolling the device with Intune.

   > [!IMPORTANT]
   > If you plan to affiliate the Surface Hub with Active Directory, the device name must meet the [standard requirements for computer names in AD](/troubleshoot/windows-server/identity/naming-conventions-for-computer-domain-site-ou#computer-names). Otherwise the setup fails.

   > [!TIP]
   > If you want to enable [Miracast over Infrastructure](miracast-over-infrastructure.md), the device name must be discoverable via DNS. You can achieve this by allowing your Surface Hub to register automatically via Dynamic DNS or manually creating an A or AAAA record for the Surface Hub's device name.

### Configure device admin accounts

You can only set up device admins during first-time Setup. For more information, see:

- [Surface Hub 2S device affiliation](/surface-hub/prepare-your-environment-for-surface-hub#device-affiliation)
- [Admin Group Management](admin-group-management-for-surface-hub.md)

1. **Choose the type of admin account**. Select one of the following options: Active Directory Domain Services, Microsoft Entra ID, or Local admin.

    :::image type="content" source="images/hub-setup-join.png" alt-text="Choose type of admin account.":::

### Active Directory Domain Services

1. If you intend to use Surface Hub in an on-premises environment, you can affiliate it with **Active Directory Domain Services**. Enter the credentials of a user with permissions to join the device to Active Directory.
2. Select the Active Directory Security Group containing members allowed to sign in to the Settings app on Surface Hub 2S.
3. Select **Finish**. The device restarts.

<a name='microsoft-azure-active-directory'></a>

### Microsoft Entra ID

1. If you intend to manage Surface Hub from the cloud using Microsoft Intune or an MDM provider, select **Microsoft Entra ID**.
2. Select Next and sign in with a work or school account. If redirected, authenticate using your organization’s sign-in page and provide more credentials if requested. Otherwise, enter your password and select **Next**.

    :::image type="content" source="images/hub-setup-signin.png" alt-text="The screenshot shows the dialog to sign in with a work or school account.":::

> [!IMPORTANT]
> Microsoft recommends that you use roles with the fewest permissions. This helps improve security for your organization. Global Administrator is a highly privileged role that should be limited to emergency scenarios when you can't use an existing role. To learn more, see the recommended guidance in [Configure non-Global Admin accounts on Surface Hub](surface-hub-2s-nonglobal-admin.md).

> [!TIP]
> To manage who can access the Settings app on Surface Hubs, make sure automatic Intune enrollment is enabled in your tenant before joining the device to Microsoft Entra ID. You can then use Intune policies to [configure non-Global admins](surface-hub-2s-nonglobal-admin.md).

### Local Administrator account

- Enter a username and a memorable password for your local admin. (If you forget the local admin password, you'll need to [recover your device](surface-hub-recover-reset.md) and repeat the setup process.)  

    :::image type="content" source="images/hub-setup-local-admin.png" alt-text="This screenshot shows the field to enter a memorable password for local admin account.":::

### Choose privacy settings for your device

- Select from the available privacy settings and select **Accept**.

    :::image type="content" source="images/hub-setup-privacy.png" alt-text="This screenshot shows the dialog to choose privacy settings.":::

### Use provisioning packages

You can customize first-time setup options to ensure a consistent experience across multiple Surface Hubs.

1. Review the documentation in [Create provisioning packages](provisioning-packages-for-surface-hub.md) and save the provisioning package to a USB thumb drive.
2. Insert the USB thumb drive into one of the USB ports when you see the License Agreement page (step 6 in the ["Get started"](#get-started) steps above).
3. When prompted, choose the provisioning package you'd like to use.
4. Follow the rest of the steps, and remove the USB drive at the first reboot that occurs in the setup process.

## Learn more

- [Prepare your environment for Surface Hub](prepare-your-environment-for-surface-hub.md)
- [Surface Hub and Microsoft Teams Rooms automated setup guide](https://go.microsoft.com/fwlink/?linkid=2221605)
