---
title: Deploy Surface app in an enterprise environment
description: Deploy the Surface app across multiple Surface devices in an enterprise environment using WinGet, Microsoft Intune, provisioning packages, or other methods. This guide covers downloading the app, preparing deployment packages, and best practices for enterprise-wide distribution.
ms.service: surface
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.localizationpriority: medium
manager: frankbu
ms.date: 02/20/2025
appliesto:
- Windows 10
- Windows 11
---

# Deploy Surface app in an enterprise environment

## Applies to:

- Surface Laptop (all generations)
- Surface Pro 3 and later
- Surface Laptop Go (all generations)
- Surface Go (all generations)
- Surface Book (all generations)
- Surface Studio (all generations)
- Surface Laptop Studio (all generations)
- Surface Pro with LTE Advanced (Model 1807)
- Surface Pro (Model 1796)
- Surface 3 LTE
- Surface 3

The Surface app is a lightweight Microsoft Store app that provides control over many Surface-specific settings and options, with quick access to device information, including the serial number, Surface model name, UEFI version, and related drivers. The Surface app comes preinstalled on Surface devices. However, if your organization is preparing images for deployment, including the Surface app in your imaging and deployment process can simplify device management.

> [!NOTE]
> This article does not apply to Surface Pro X or Surface Pro 9 with 5G. For more information, see [Deploy, manage, and service ARM-based Surface devices](surface-pro-arm-app-management.md).

## Options to download and deploy Surface app

Use one of the following package types to deploy:

- [Deploy using MSIX package](#deploy-using-msix-package)
- [Download Appx package](#download-appx-package)
- [Download and deploy via WinGet](#download-and-deploy-via-winget)

Then, choose a deployment method:

- [Deploy via Microsoft Intune or a provisioning pack](#deploy-via-intune-or-a-provisioning-pack)

### Deploy using MSIX package

1. **Download the [Surface app MSIX bundle](https://www.microsoft.com/en-my/download/details.aspx?id=105302)** from the Microsoft Download Center.

The MSIX packaging format is a modern replacement for Appx, offering enhanced features such as improved security, support for application customization, and easier integration with existing IT management tools. MSIX packages bundle all necessary components and dependencies, simplifying deployment and reducing the likelihood of installation issues due to missing files. MSIX is ideal for enterprise environments where reliability and ease of management are priorities.

2. **Install using PowerShell**:
    - Open PowerShell with administrative privileges.
    - Navigate to the directory where the MSIX bundle is stored.
    - Run the following command to install the bundle:

      ```powershell
      Add-AppPackage -Path .\SurfaceAppPackage_74.7180.129.0_x64_arm64.msixbundle
      ```

   - Or you can deploy using other methods that accept the MSIX bundle format.

### Download Appx package

Choose the Appx package if your environment relies on legacy systems or established workflows optimized for Appx compatibility. This ensures smooth integration across devices, especially in cases where MSIX adoption is not yet feasible.

### Download and deploy via WinGet

WinGet, also known as the Windows Package Manager, simplifies software management on Windows devices. With the retirement of the Microsoft Store for Business, WinGet provides organizations a flexible way to manage applications on Surface devices and other PCs. By using WinGet, IT admins can browse the repository of available applications, install necessary software, and automate some app management tasks.

#### Install WinGet

1. By default, WinGet is preinstalled on Windows 10 (version 1809 and later) and Windows 11. To confirm you have WinGet installed, open a command prompt and enter **winget**.
2. Ensure you're running WinGet 1.8 or later.
3. If WinGet isn't present or you need the latest version, follow these instructions: [Install WinGet](/windows/package-manager/winget/#install-winget).

#### Download Surface app via WinGet

1. Enter the following command and agree to the terms:

    ```powershell
    winget install --id 9WZDNCRFJB8P --accept-package-agreements --accept-source-agreements
    ```

2. When the download completes, view the files in a newly created subdirectory in your Downloads folder. The Store app ID of the Surface app is **9WZDNCRFJB8P** and is also the name of the subdirectory containing the files.

### Install with PowerShell

1. **Open PowerShell with administrative privileges**:
   - Press `Win + X` and select **Windows PowerShell (Admin)** or **Windows Terminal (Admin)** from the menu. This opens an elevated PowerShell session, which is necessary for installing app packages.

2. **Navigate to the directory**:
   - Use the `cd` command to navigate to the directory where your Appxbundle file is located. For example:

     ```powershell
     cd C:\Temp
     ```

3. **Run the installation command**:
   - Use the `Add-AppxPackage` cmdlet to install the Appxbundle file. Replace `<DownloadPath>` with the actual path to your file:

     ```powershell
     Add-AppxPackage -Path "<DownloadPath>\Microsoft.Surface_10.0.342.0_neutral_~_8wekyb3d8bbwe.AppxBundle"
     ```

   - For example, if the file is located in `C:\Temp`, use the following command:

     ```powershell
     Add-AppxPackage -Path "C:\Temp\Microsoft.Surface_10.0.342.0_neutral_~_8wekyb3d8bbwe.AppxBundle"
     ```

4. **Verify the installation** by checking if the Surface app appears in the Start menu or by using the following PowerShell command:

     ```powershell
     Get-AppxPackage | Select Name, PackageFullName
     ```

### Deploy via Intune or a provisioning pack

To deploy the Surface app across multiple devices in an enterprise environment, use Microsoft Intune or provisioning packages. These methods support bulk deployment and simplify app updates. For more information, see the following resources:

- [Add a Windows line-of-business app to Microsoft Intune](/mem/intune/apps/lob-apps-windows)
- [Provision PCs with apps](/windows/configuration/provisioning-packages/provision-pcs-with-apps)
- [Distribute LOB apps to enterprises](/windows/apps/publish/distribute-lob-apps-to-enterprises)

