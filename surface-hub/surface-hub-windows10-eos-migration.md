---
title: End of support options and migration paths for Surface Hub v1 and 2S devices running Windows 10 Team edition
description: Surface Hub 2S must migrate from Windows 10 by October 14, 2025. Learn about upgrade options and Microsoft Teams app support changes.
ms.reviewer: dpandre
manager: frankbu
ms.service: surface-hub
author: coveminer
ms.author: chauncel 
ms.topic: how-to
ms.date: 04/14/2025
ms.localizationpriority: medium
---

# End of support options and migration paths for Surface Hub v1 and 2S devices running Windows 10 Team edition

This article provides step-by-step guidance for Surface Hub v1 and 2S customers affected by the Windows 10 Team edition end of support. It explains available options based on your current configuration and highlights key dates, actions, and technical pathways to maintain a supported and functional device.

> [!IMPORTANT]
> The [free seamless software migration offering service](surface-hub-2s-migrate-to-mtr-w.md) for Surface Hub 2S is available until October 14, 2025. After this date, migrating your device requires a [more manual process using Surface Enterprise Management Mode (SEMM)](surface-hub-2s-migrate-os.md). We strongly recommend completing the software migration now to avoid extra steps and ensure a smooth transition.
>
> **Note:** Unlike standard Windows 10 editions, Windows 10 Team doesn't have an extended support option beyond this date.

## End of support overview

- Windows 10 Team edition reaches end of support on **October 14, 2025**.
- Surface Hub 2S devices must be on a Windows 11-based platform, such as [Microsoft Teams Rooms on Windows](surface-hub-2s-migrate-to-mtr-w.md), in order to continue receiving updates and support. 
- Surface Hub v1 devices will no longer be supported. It's recommended to upgrade to a newer Surface Hub device. 
- Microsoft Teams Rooms and the [Teams Rooms Pro Management Portal](/microsoftteams/rooms/managed-meeting-rooms-portal) will also stop supporting Windows 10 after this date.
- The Microsoft Teams app (that preceded Microsoft Teams Rooms on Windows) has been deprecated and will no longer be accessible on **Surface Hub v1** and **Surface Hub 2S** devices running Windows 10 Team edition after October 14, 2025. To learn more, see [Microsoft Teams App End of Availability on Surface Hub v1 and 2S Running Windows 10 Team edition](/microsoftteams/rooms/rooms-lifecycle-support#microsoft-teams-app-end-of-availability-on-surface-hub-v1-and-2s-running-windows-10-team-edition).


## What this means for your organization

- Surface Hub devices that remain on Windows 10 Team edition will no longer be supported or receive security updates.
- Organizations using Teams on Surface Hub running an unsupported OS will need to transition to supported solutions.

## Recommended transition paths

### For Surface Hub v1

- Microsoft recommends planning for a hardware refresh such as upgrading to [Surface Hub 3](surface-hub-3-whats-new.md) to maintain a secure and
supported Teams experience.​ 

### For Surface Hub 2S

Surface Hub 2S devices should transition to a supported Windows 11-based platform to continue using Teams and receive the latest updates. You have three options:

1. **Hardware upgrade**:
   - The easiest path is to install the [Surface Hub 3 Compute Cartridge](install-manage-surface-hub-3-compute-cartridge.md), which comes preloaded with the Windows 11-based Microsoft Teams Rooms on Windows platform. This cartridge also provides the best experience of Teams Rooms on Surface Hub due to the enhanced performance capabilities of Surface Hub 3 ([as detailed in this blog post](https://techcommunity.microsoft.com/blog/surfaceitpro/now-available-surface-hub-2s-migration-to-microsoft-teams-rooms-on-windows/4064081#community-4064081-surface-hub-2s-migration-reminders)).

2. **Software migration** *(available only until October 14, 2025)*:
   - Surface Hub 2S devices can also be software-migrated to the Microsoft Teams Rooms platform using the process outlined in [Migrate Surface Hub 2S to Microsoft Teams Rooms on Windows](surface-hub-2s-migrate-to-mtr-w.md).

3. **Convert to Windows 11 Pro or Enterprise**:
   - Unlock the device, then install a supported Windows 11 Pro or Enterprise image as described in [Migrate to Windows 10/11 Pro or Enterprise on Surface Hub 2S](surface-hub-2s-migrate-os.md). 

## Learn more

- [Windows 10 Team (Surface Hub) - Microsoft Lifecycle](/lifecycle/products/windows-10-team-surface-hub)