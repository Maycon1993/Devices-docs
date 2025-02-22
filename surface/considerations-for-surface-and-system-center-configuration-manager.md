---
title: Considerations for Surface and Microsoft Configuration Manager
description: Deploy and manage Surface devices with Configuration Manager, including drivers, licensing, security, and Windows 11 updates.
ms.service: surface
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.localizationpriority: medium
manager: frankbu
ms.date: 11/05/2024
appliesto:
- Windows 10
- Windows 11
---

# Considerations for Surface and Microsoft Configuration Manager

Fundamentally, management and deployment of Surface devices with Microsoft Configuration Manager follows the same principles as managing other PCs. Like any PC deployment, it includes importing drivers, preparing Windows images, setting deployment task sequences, and applying those sequences to device collections. After deployment, Surface devices behave like any other Windows client, receiving apps, settings, and policies through familiar processes.

To learn more, see [Microsoft Configuration Manager documentation](/mem/configmgr/).

Although the deployment and management of Surface devices is fundamentally similar to other PCs, some scenarios might require extra IT tasks, as described in this article.

## Proactive monitoring, security, and AI-powered insights

Configuration Manager supports enhanced security, proactive monitoring, and compliance enforcement. It enables IT administrators to take advantage of **virtualization-based security (VBS)** to isolate critical security operations, while **TPM 2.0** plays a foundational role in enabling **encryption with BitLocker**, **secure boot**, and **Windows Hello for Business**. Configuration Manager ensures compliance with these security baselines by monitoring device health and policy adherence, ensuring devices are protected against unauthorized access.

Additionally, [Microsoft Defender for Endpoint](/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection) integrates with Configuration Manager, delivering AI-powered threat detection and response capabilities, helping organizations detect anomalies and protect against sophisticated threats.

## Windows 11 24H2 Update integration

Ensure compatibility by using Configuration Manager for **Windows 11 24H2 deployments** on Surface devices. Ensure product activation is aligned when deploying or reimaging these devices  using **OEM Activation 3.0 (OA 3.0)** tools or **Microsoft’s KMS infrastructure**.

- **Key resources**: Check the **Windows Setup Edition Configuration and Product ID Files** for licensing requirements. When installing or reimaging with Windows Enterprise editions, use the proper task sequences to avoid conflicts between the embedded firmware key and the new OS.

## Surface Ethernet adapters and Configuration Manager deployment

When deploying Surface devices using Ethernet adapters, Configuration Manager identifies devices by **MAC address**. However, shared Ethernet adapters can cause deployment issues by recognizing multiple devices as a single device. To avoid this, configure Configuration Manager to use alternative identifiers, such as the **System UUID**.

- **Best practice**: Exclude Surface Ethernet adapters from MAC-based identification to prevent deployment conflicts.
- **Driver availability**: Drivers for older Windows versions are available in the [Microsoft Update Catalog](https://www.catalog.update.microsoft.com/Search.aspx?q=surface%20ethernet%20drivers). For newer versions, the drivers are included by default in Windows and require no extra configuration.

## Use prestaged media with Surface clients

If using **prestaged media** for Surface deployments, take extra steps to accommodate UEFI environments requiring multiple partitions. To learn more, see [Create prestaged media](/mem/configmgr/osd/deploy-use/create-prestaged-media).

## Licensing conflicts with OEM Activation 3.0

Surface devices ship with an embedded **Windows license key** via **OEM Activation 3.0**. Be aware of potential conflicts when deploying Windows editions that differ from the preinstalled OS.

- **Example**: If a device ships with **Windows 11 Home** and you want to install **Windows 11 Pro**, use an **Ei.cfg** or **Pid.txt** file to bypass the embedded license key.
- **Enterprise deployment**: For organizations using **Windows Enterprise** editions, the embedded key is bypassed by default, and **KMS or Active Directory-based activation** completes the process.

## Apply an asset tag during deployment

Use the [Surface Asset Tag Tool](surface-it-toolkit-library.md) to apply asset tags directly from UEFI. This allows identification even if the OS fails, streamlining asset management for IT admins. To learn more, see [Introduction to asset intelligence in Configuration Manager](/mem/configmgr/core/clients/manage/asset-intelligence/introduction-to-asset-intelligence).

## Configure push-button reset

By default, **push-button reset** restores Surface devices to a clean state, discarding apps and settings. For professional environments, configure push-button reset to restore devices with preinstalled configurations using [Deploy push-button reset features](/windows-hardware/manufacture/desktop/deploy-push-button-reset-features).
