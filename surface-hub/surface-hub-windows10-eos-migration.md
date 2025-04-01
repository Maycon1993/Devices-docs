---
title: Surface Hub-End of support options and migration paths
description: How to keep using Surface Hub after Windows 10 end of support with guidance on Teams app support, migration deadlines, and upgrade options.
ms.reviewer: dpandre
manager: frankbu
ms.service: surface-hub
author: coveminer
ms.author: 
ms.topic: how-to
ms.date: 09/24/2024
ms.localizationpriority: medium
---

# Surface Hub: End of support options and migration paths

This article provides step-by-step guidance for Surface Hub customers affected by the Windows 10 Team Edition end of support (end of support). It explains available options based on your current configuration and highlights key dates, actions, and technical pathways to maintain a supported and functional device.

## End of support overview

- Windows 10 Team Edition reaches end of support on **October 14, 2025**.
- Devices still running Team Edition must be migrated to continue receiving updates and support.
- The Microsoft Teams 1.0 client is deprecated; devices relying on it are no longer functional.
- Microsoft Teams Rooms and Teams Rooms Pro Management software will also stop supporting Windows 10 after this date.
- The Microsoft Teams app will no longer be accessible on **Surface Hub v1** and **Surface Hub 2S** devices running Windows 10 Team Edition.

> [!IMPORTANT]
> Action may be required by **November 13, 2025**, to ensure devices continue functioning as expected.
>
> **The free seamless software migration service for Surface Hub 2S will no longer be available after October 14, 2025.** After this date, migrating your device will require a [more manual process using the Surface Enterprise Management Mode (SEMM) tool](/surface/surface-enterprise-management-mode). We strongly recommend completing the software migration before this deadline to avoid extra steps and ensure a smooth transition. 
>
> **Note:** Unlike standard Windows 10 editions, Windows 10 Team doesn't have an extended support option beyond this date.

## What this means for your organization

- Surface Hub devices that remain on Windows 10 Team Edition will no longer be supported or receive security updates.
- Organizations using Teams on Surface Hub running an unsupported OS will need to transition to supported solutions.

## Recommended transition paths

### For Surface Hub v1

- Microsoft recommends transitioning to alternative collaboration solutions or upgrading to newer hardware, such as **Surface Hub 3**.

### For Surface Hub 2S

Surface Hub 2S devices should transition to a supported Windows 11-based platform to continue using Teams and receive the latest updates. You have three options:

1. **Hardware upgrade**:
   - The easiest path is to install a **[Surface Hub 3 Compute Cartridge](surface-hub-3-compute-cartridge-overview.md)**, which comes preloaded with the Windows 11-based Microsoft Teams Rooms on Windows platform. This cartridge also provides the best experience of Teams Rooms on Surface Hub due to the unique hardware capabilities of Surface Hub 3 ([as detailed at the end of this blog post](https://techcommunity.microsoft.com/t5/surface-it-pro-blog/what-s-new-for-surface-hub-3/ba-p/3962801)).

2. **Software migration** *(available only until October 14, 2025)*:
   - Surface Hub 2S devices can also be software-migrated to the Microsoft Teams Rooms platform using the process outlined in the [Surface Hub 2S OS migration guide](surface-hub-2s-migrate-os). 

3. **Convert to Windows 11 Pro or Enterprise**:
   - Use the migration process to unlock the device and install a supported Windows 11 Pro or Enterprise image ([Learn more](/windows/whats-new/windows-11-requirements)).

## Option 1: Migrate to Microsoft Teams Rooms on Windows

### Recommended for customers who:

- Want to continue using the device in a managed meeting room scenario
- Are migrating after end of support

### Migration steps:

1. Unlock the device using the process outlined in the [Surface Hub 2S OS migration guide](surface-hub-2s-migrate-os.md).
2. Apply a **BMR (bare metal recovery) image** to install Microsoft Teams Rooms on Windows.

> [!NOTE]
> After migration, the device remains unlocked and can be reimaged as needed.

> [!IMPORTANT]
> The Windows 10/11 Pro or Enterprise + BMR migration offering is supported only through **October 14, 2025**.

## Option 2: Convert to standard Windows 10/11 Pro or Enterprise

### Suitable for:

- Organizations needing a general-purpose Windows device
- Customers not intending to use Microsoft Teams Rooms

### Conversion steps:

1. Unlock the device using the same process described in the migration guide.
2. Apply a supported Windows 10/11 Pro or Enterprise image.

> [!IMPORTANT]
> Activation services for Surface Hub 2S will remain available through **January 11, 2027**, to support recovery and reimaging scenarios.

## Other best practices

- The previously available "easy" migration path is no longer supported.
- Devices that have already been migrated don't need to repeat the migration process.
- Post-migration, devices can be freely reimaged to Teams Rooms or other supported Windows editions.
- **BMR remains the long-term recovery method** for Surface Hub 2S devices on a supported OS.
- OS version **10.0.19045 or lower** must be upgraded.
- Devices not compatible with Windows 11 due to processor limitations (for example, some Lenovo, HP, Yealink, Crestron models) may require replacement.

## Tools to assist

- Use the [Windows 11 readiness checker](/windows/whats-new/windows-11-requirements) to verify upgrade compatibility.
- Use Teams Rooms Pro Management portal Room Inventory to identify devices needing action.
