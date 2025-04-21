---
title: Manage & deploy Surface driver & firmware updates 
description: Learn how to manage and deploy Surface driver and firmware updates, with links to downloadable .msi packages and guidance for enterprise environments.
ms.assetid: CD1219BA-8EDE-4BC8-BEEF-99B50C211D73
manager: frankbu
ms.localizationpriority: medium
ms.service: surface
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.date: 04/21/2025
appliesto:
- Windows 10
- Windows 11
---

# Manage & deploy Surface driver & firmware updates

How you manage Surface driver and firmware updates depends on your environment and organizational requirements. IT admins in larger organizations often stage deployments and conduct testing before rolling out updates to users, ensuring systems remain stable and secure.

> [!NOTE]
> This article is intended for IT professionals and applies to Surface devices only. For home users looking to install updates, see [Download drivers and firmware for Surface](https://support.microsoft.com/help/4023505).

Centrally managing updates remains essential for maintaining secure, up-to-date systems. This reduces downtime, ensures Surface devices are protected with the latest security patches, and keeps firmware in sync with new features introduced via Windows updates.

## What's included in Surface driver and firmware updates

Windows Installer .msi files contain all the required cumulative driver and firmware updates for Surface devices. Update packages might include some or all of the following components:

- Wi-Fi and LTE
- Video
- Solid-state drive
- System Aggregator Module (SAM)
- Battery
- Keyboard controller
- Embedded controller (EC)
- Management engine (ME) – Applies to Intel-based Surface devices
- Unified Extensible Firmware Interface (UEFI)

## Download and install updates

1. Choose either **Windows 11** or **Windows 10** as appropriate for your organization.  
2. If multiple .msi files are available, select the file corresponding to your Surface model and deployed OS version.  

> [!IMPORTANT]
> When Windows 10 reaches end of support on October 14, 2025, Microsoft will no longer release security updates, bug fixes, time zone updates, or provide technical support. To learn more, including transition options for organizations needing more time, see [Plan for Windows 10 End of Support with Windows 11, Windows 365, and ESU](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/plan-for-windows-10-eos-with-windows-11-windows-365-and-esu/ba-p/4000414).

> [!NOTE]
> Surface Pro 11th Edition with Intel processor, Surface Pro 10 with 5G, and Surface Laptop 7th Edition with Intel processor now support deployment with Windows 11, version 23H2. Factory images for Windows 11 23H2 are not available. Organizations must download and install the OS themselves and integrate the MSI driver and firmware package into their imaging solution. While Windows 11 23H2 expands deployment flexibility, some features supported in Windows 11 24H2 are not available in 23H2.

| Surface device                                                                                                                                        | Downloadable .msi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Surface Pro**                                                                                                                                       | - [Surface Pro 11th Edition, Intel processor](https://www.microsoft.com/download/details.aspx?id=108013&msockid=28a850520e226efc1ba245090f0f6f14)<br>- [Surface Pro 11th Edition, Snapdragon processor](https://www.microsoft.com/download/details.aspx?id=106119)<br>- [Surface Pro 10](https://www.microsoft.com/download/details.aspx?id=105947)<br>- [Surface Pro 10 with 5G](https://www.microsoft.com/en-us/download/details.aspx?id=106292)<br>- [Surface Pro 9 with Intel processor](https://www.microsoft.com/download/details.aspx?id=104680)<br>- [Surface Pro 9 with 5G (SQ3 processor)](https://www.microsoft.com/download/details.aspx?id=105941)<br>- [Surface Pro 8](https://www.microsoft.com/download/details.aspx?id=103503)<br>- [Surface Pro 7+ and Surface Pro 7+ (LTE)](https://www.microsoft.com/download/details.aspx?id=102633)<br>- [Surface Pro 7](https://www.microsoft.com/download/details.aspx?id=100419)<br>- [Surface Pro 6](https://www.microsoft.com/download/details.aspx?id=57514)<br>- [Surface Pro 5 (LTE)](https://www.microsoft.com/download/details.aspx?id=56278)<br>- [Surface Pro 5 (Wi-Fi)](https://www.microsoft.com/download/details.aspx?id=55484)<br>- [Surface Pro 4](https://www.microsoft.com/download/details.aspx?id=49498)<br>- [Surface Pro 3](https://www.microsoft.com/download/details.aspx?id=38826)<br>- [Surface Pro 2](https://www.microsoft.com/download/details.aspx?id=49042)<br>- [Surface Pro](https://www.microsoft.com/download/details.aspx?id=49038) |
| **Surface Laptop**                                                                                                                                    | - [Surface Laptop 7th Edition, Intel processor](https://www.microsoft.com/download/details.aspx?id=108014)<br>- [Surface Laptop 7th Edition, Snapdragon processor](https://www.microsoft.com/download/details.aspx?id=106120)<br>- [Surface Laptop 6](https://www.microsoft.com/download/details.aspx?id=105946)<br>- [Surface Laptop 5](https://www.microsoft.com/download/details.aspx?id=104679)<br>- [Surface Laptop 4 with Intel processor](https://www.microsoft.com/download/details.aspx?id=102924)<br>- [Surface Laptop 4 with AMD processor](https://www.microsoft.com/download/details.aspx?id=102923)<br>- [Surface Laptop 3 with Intel processor](https://www.microsoft.com/download/details.aspx?id=100429)<br>- [Surface Laptop 3 with AMD processor](https://www.microsoft.com/download/details.aspx?id=100428)<br>- [Surface Laptop 2](https://www.microsoft.com/download/details.aspx?id=57515)<br>- [Surface Laptop](https://www.microsoft.com/download/details.aspx?id=55489)                                                                                                                                                                                    |
| **Surface Laptop Go**                                                                                                                                 | - [Surface Laptop Go 3](https://www.microsoft.com/download/details.aspx?id=105608)<br>- [Surface Laptop Go 2](https://www.microsoft.com/download/details.aspx?id=104251)<br>- [Surface Laptop Go](https://www.microsoft.com/download/details.aspx?id=102261)<br>                                                                                                                                                                                   |
| **Surface Laptop Studio**                                                                                                                             | - [Surface Laptop Studio 2](https://www.microsoft.com/download/details.aspx?id=105610)<br>- [Surface Laptop Studio](https://www.microsoft.com/download/details.aspx?id=103505)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Surface Book**                                                                                                                                      | - [Surface Book 3](https://www.microsoft.com/download/details.aspx?id=101315)<br>- [Surface Book 2](https://www.microsoft.com/download/details.aspx?id=56261)<br>- [Surface Book](https://www.microsoft.com/download/details.aspx?id=49497)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Surface Go**                                                                                                                                        | - [Surface Go 4](https://www.microsoft.com/download/details.aspx?id=105609)<br>- [Surface Go 3](https://www.microsoft.com/download/details.aspx?id=103504)<br>- [Surface Go 2](https://www.microsoft.com/download/details.aspx?id=101304)<br>- [Surface Go (Wi-Fi)](https://www.microsoft.com/download/details.aspx?id=57439)<br>- [Surface Go (LTE)](https://www.microsoft.com/download/details.aspx?id=57601)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Surface Studio**                                                                                                                                    | - [Surface Studio 2+](https://www.microsoft.com/download/details.aspx?id=104681)<br>- [Surface Studio 2](https://www.microsoft.com/download/details.aspx?id=57593)<br>- [Surface Studio](https://www.microsoft.com/download/details.aspx?id=54311)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Surface 3**                                                                                                                                         | - [Surface 3 (Wi-Fi)](https://www.microsoft.com/download/details.aspx?id=49040)<br>- [Surface 3 (LTE) - ATT](https://www.microsoft.com/download/details.aspx?id=49039)<br>- [Surface 3 (LTE) - Verizon](https://www.microsoft.com/download/details.aspx?id=49920)<br>- [Surface 3 (LTE) - Outside of North America and Y!mobile in Japan](https://www.microsoft.com/download/details.aspx?id=49041)                                                                                                                                                                                                                                                                                                                                                   |
| **Surface Hub running**  [**Windows 10 Pro or Windows 10 Enterprise**](/surface-hub/surface-hub-2s-migrate-os) | - [Windows 10 Pro and Enterprise OS on Surface Hub 2S](https://www.microsoft.com/download/details.aspx?id=101974)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Surface Hub running Windows 10 Teams 2020 Update**                                                                                                  | - See [Manage Windows updates on Surface Hub](/surface-hub/manage-windows-updates-for-surface-hub)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Surface Dock**                                                                                                                                      | - [Surface Thunderbolt 4 Dock](https://www.microsoft.com/download/details.aspx?id=105115)<br>- [Surface Dock 2](https://www.microsoft.com/download/details.aspx?id=101317)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

### Installation guidance for Surface devices

- **Windows Update**: Surface devices can automatically receive driver and firmware updates via Windows Update, helping ensure security with minimal admin intervention.
- **Surface MSI packages**: Useful for testing and controlled deployments. Download and install updates from the [links on this page](#download-and-install-updates).

> [!TIP]
> Automating updates through **Windows Update for Business** ensures firmware and driver updates align with security patches, reducing the need for manual interventions.

## Centralized management tools

### Microsoft Intune and Configuration Manager

- **Intune**: Manage Surface firmware updates remotely using Intune and the **Surface Management Portal** for visibility into device status. The portal provides a consolidated view of all Surface devices across the organization.
  
- **Configuration Manager**: Synchronize Surface firmware and driver updates with Configuration Manager for on-premises management. Use Configuration Manager to automate deployments or co-manage devices via **Microsoft Entra hybrid join**. To learn more, see [Configure Microsoft Entra hybrid join](/entra/identity/devices/how-to-hybrid-join).

**Helpful resources:**

- [Manage Surface driver updates in Configuration Manager](/mem/configmgr/sum/deploy-use/surface-drivers)
- [Surface Management Portal Overview](/mem/intune/fundamentals/surface-management-portal)

## Security benefits of driver and firmware updates

Keeping drivers and firmware up to date ensures:

- **Enhanced security**: Regular updates reduce vulnerabilities by addressing firmware-level risks.
- **Improved performance**: Drivers aligned with the latest OS updates ensure the best experience.
- **Simplified management**: Using tools like Intune and the Surface Management Portal ensures seamless deployment and tracking of updates, reducing administrative overhead.  

### Best practices for firmware updates

- **Test updates in stages**: Deploy updates to a test group first before rolling them out organization-wide.
- **Monitor device health**: Use Intune’s **Surface Management Portal** to track update success and detect any issues. To learn more, see [Surface Management Portal overview](surface-management-portal.md). 
- **Adopt Windows Update for Business**: This ensures Surface devices always have the latest drivers, firmware, and security patches. To learn more, see [Configure Windows Update for Business](/windows/deployment/update/waas-configure-wufb).

## Managing firmware with DFCI


By having Device Firmware Configuration Interface (DFCI) profiles [built into Intune](/mem/intune/configuration/device-firmware-configuration-interface-windows), Surface UEFI management extends the modern management stack down to the UEFI hardware level. DFCI supports zero-touch provisioning, eliminates BIOS passwords, provides control of security settings (including startup options and built-in peripherals), and lays the groundwork for advanced security scenarios in the future. For more information, see the following resources:

## Automate driver and firmware updates with MDT on Windows 10

While the [Microsoft Deployment Toolkit (MDT)](/previous-versions/windows/it-pro/windows-10/deployment/deploy-windows-mdt/get-started-with-the-microsoft-deployment-toolkit) isn’t supported for ARM-based devices or Windows 11, it remains a useful tool for automating updates on x86-based Surface devices running Windows 10. Use task sequences to install drivers and updates during OS deployment, ensuring devices are up to date from the start. To learn more, see [Task Sequence Steps](/mem/configmgr/mdt/task-sequence-steps).

## Surface .msi naming convention

Since August 2019, .msi files follow this convention:

**Product**\_**Windows release**\_**Windows build number**\_**Version number**\_**Revision of version number (typically zero)**

### Example

- **SurfacePro11_Win11_26100_24.091.12892.0.msi**

This filename provides the following information:

- **Product**: Surface Pro 11th Edition, Snapdragon processor  
- **Windows release**: Win11  
- **Build**: 26100  
- **Version**: 24.091.12892 – This version number reveals the following:
  - **Year**: 24 (2024)  
  - **Month and week**: 091 (first week of September)  
  - **Minute of the month**: 12892  
- **Revision of version**: 0 (first release of this version)

This helps IT admins select the correct update based on product, OS, and build compatibility.

## Learn more

- [Manage Surface driver updates in Configuration Manager](/mem/configmgr/sum/deploy-use/surface-drivers)  
- [Deploy applications with Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-applications)  
- [Surface Management Portal Overview](/mem/intune/fundamentals/surface-management-portal)  
- [Plan for Windows 10 End of Support](https://techcommunity.microsoft.com/t5/windows-it-pro-blog/plan-for-windows-10-eos-with-windows-11-windows-365-and-esu/ba-p/4000414)
