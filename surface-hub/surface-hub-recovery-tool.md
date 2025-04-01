---
title: Use the Surface Hub Recovery Tool for Surface Hub v1
description: Use the Surface Hub Recovery Tool to reimage the SSD on Surface Hub v1, fix boot issues, or recover from lost admin access.
ms.assetid: FDB6182C-1211-4A92-A930-6C106BCD5DC1
manager: frankbu
ms.service: surface-hub
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.date: 03/31/2025
ms.localizationpriority: medium
appliesto:
- Surface Hub
---

# Use the Surface Hub Recovery Tool for Surface Hub v1

[!INCLUDE [Hub 2S EoS](includes/hub2s-eos.md)]

The [Microsoft Surface Hub Recovery Tool](https://www.microsoft.com/download/details.aspx?id=52210) helps you reimage your Surface Hub Solid State Drive (SSD) from a separate PC without replacing the SSD or calling support. Use this tool for any of the following scenarios:

- You're unable to use [local reset option](device-reset-surface-hub.md).
- You need to reimage an SSD that has an older version of the operating system.
- You no longer have access to the Administrator password.
- You're encountering boot errors that prevent restarting Surface Hub.

> [!NOTE]
> The tool won't fix physically damaged SSDs.

To reimage the Surface Hub SSD using the Recovery Tool, you need to remove the SSD from the Surface Hub and connect the drive to the USB-to-SATA cable. Next, connect the cable to the desktop PC on which the Recovery Tool is installed. For more information on how to remove the existing drive from your Surface Hub, see [Surface Hub SSD replacement](surface-hub-ssd-replacement.md).

> [!IMPORTANT]
> Don't let the device go to sleep or interrupt the download of the image file.

If the tool is unsuccessful in reimaging your drive, contact [Surface Hub Support](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).

## Prerequisites

### Mandatory

- Host PC running 64-bit version of Windows 10, version 1607 or later.
- An Internet connection
- An available USB 2.0 or later port
- USB-to-SATA cable
- 10 GB of free disk space on the host computer
- SSDs shipped with Surface Hub or an SSD provided by Support as a replacement. SSDs not supplied by Microsoft aren't supported.

### Recommended

- High-speed Internet connection
- Open USB 3.0 port
- USB 3.0 or later USB-to-SATA cable
- The imaging tool was tested with the following make and model of cables:
  - Startech USB312SAT3CB
  - Rosewill RCUC16001
  - Ugreen 20231

## Download Surface Hub Recovery Tool

The Surface Hub Recovery Tool is available for download from [Surface Hub Tools for IT](https://www.microsoft.com/download/details.aspx?id=52210)  under the filename **SurfaceHub_Recovery_v2.7.139.0.msi**.

To start the download, select **Download**, choose **SurfaceHub_Recovery_v2.7.139.0.msi**  from the list, and select **Next**. From the pop-up, choose one of the following options:

- Select **Run** to start the installation immediately.
- Select **Save** to copy the download to your computer for later installation.

Install Surface Hub Recovery Tool on the host PC.

## Run Surface Hub Recovery Tool

1. On the host PC, select the **Start** button, scroll through the alphabetical list on the left, and select the recovery tool shortcut.

   :::image type="content" source="images/shrt-shortcut.png" alt-text="Screenshot of Microsoft Surface Hub Recovery Tool shortcut." :::

2. Select **Start**.

   :::image type="content" source="images/shrt-start.png" alt-text="Screenshot of Recovery Tool Start button." :::

3. In the **Guidance** window, select **Next**.

   :::image type="content" source="images/shrt-guidance.png" alt-text="Screenshot of Don't let your machine go to sleep guidance." :::

4. In the Select image window, select either **20H2** or its successor **22H2**, select **Continue**, and then select **Download image**.

   :::image type="content" source="images/shrt-select-image.png" alt-text="Screenshot of Recovery Tool Select image." :::
   :::image type="content" source="images/shrt-download-image.png" alt-text="Screenshot showing image download." :::

5. Download time depends on Internet speed. On an average corporate connection, it can take up to an hour to download the 8 GB image.

   :::image type="content" source="images/shrt-download.png" alt-text="Screenshot showing progress of image download." :::

6. After the download completes, the tool will prompt you to connect an SSD. If it can't detect the drive, the issue is often due to the cable not reporting the SSD name to Windows. The imaging tool requires the drive to appear as "LITEON L CH-128V2S USB Device" to proceed. For more information on how to remove the existing drive from your Surface Hub, see [Surface Hub SSD replacement](surface-hub-ssd-replacement.md).

   :::image type="content" source="images/shrt-drive.png" alt-text="Screenshot of Connect SSD." :::

7. When the drive is recognized, select **Start** to begin the reimaging process. On the warning that all data on the drive will be erased, select **OK**.

Before the system image is applied, the SSD is repartitioned and formatted. Copying system binaries typically takes about 30 minutes, but may take longer depending on USB bus speed, cable quality, or installed antivirus software. 

## Troubleshooting and common problems

Issue | Notes
--- | ---
The tool fails to image the SSD | Make sure you're using a factory-supplied SSD and one of the tested cables.
The reimaging process appears halted/frozen | It's safe to close and restart the Surface Hub Recovery Tool with no ill effect to the SSD.
The drive isn’t recognized by the tool | Verify that the Surface Hub SSD is enumerated as a Lite-On drive, "LITEON L CH-128V2S USB Device".  If the drive is recognized as another named device, your current cable isn’t compatible. Try another cable or one of the tested cables listed on this page.
Error: -2147024809 | Open Disk Manager and remove the partitions on the Surface Hub drive.  Disconnect and reconnect the drive to the host machine. Restart the imaging tool again.

If the tool is unsuccessful in reimaging your drive, contact [Surface Hub Support](https://support.microsoft.com/help/4037644/surface-contact-surface-warranty-and-software-support).

## Version history

### Version v2.7.139.0

This version of Surface Hub Recovery Tool adds support for Windows 10 Team 2022 Update (22H2).

### Version v2.0.139.0

> [!IMPORTANT]
> This version is no longer functional. Download the current version.
