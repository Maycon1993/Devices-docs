---
title: Deploy Surface app in enterprise environments
description: Guide for deploying the Surface app across multiple Surface devices in an enterprise environment using Microsoft Intune, WinGet, or provisioning packages.
ms.service: surface
author: coveminer
ms.author: chauncel
ms.topic: how-to 
ms.localizationpriority: medium
manager: frankbu
ms.date: 11/13/2024
appliesto:
- Windows 10
- Windows 11
---

# Deploy Surface app in enterprise environments

With the retirement of the Microsoft Store for Business, this article outlines modern methods to deploy the Surface app across multiple devices in an enterprise setting. Deployment can be accomplished using Microsoft Intune, WinGet, or provisioning packages. This article provides an overview of these options and links to detailed resources for each approach.

> [!NOTE]
> This article does not apply to Surface Pro X or Surface Pro 9 with 5G. For details, see [Deploy, manage, and service ARM-based Surface devices](surface-pro-arm-app-management.md).

## Deployment options for Surface app

### Deploy with Microsoft Intune

For managed deployment, use Microsoft Intune to add and manage the Surface app on devices across your organization. Intune supports app updates and configuration, ensuring all Surface devices have the latest app version.

- For detailed steps, see [Add a Windows line-of-business app to Microsoft Intune](/mem/intune/apps/lob-apps-windows).

### Deploy using WinGet

WinGet (Windows Package Manager) offers command-line installation and management capabilities, making it ideal for organizations needing flexible, scriptable deployment options. WinGet provides an alternative to the retired Store for Business, supporting bulk deployments across Surface devices.

- To learn more, see [Install and use WinGet](/windows/package-manager/winget/).

### Provisioning packages

For organizations not using centralized management, provisioning packages allow you to include the Surface app as part of the device setup process. This method is useful for IT teams deploying custom Windows images or setting up devices offline.

- For guidance on creating provisioning packages, see [Provision PCs with apps](/windows/configuration/provisioning-packages/provision-pcs-with-apps).
