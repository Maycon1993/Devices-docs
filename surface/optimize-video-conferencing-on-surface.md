---
title: Optimize video conferencing on Surface devices
description: Optimize video conferencing on Surface devices with tips for Microsoft Teams, including driver updates, power settings, and performance best practices.
ms.service: windows-11
ms.localizationpriority: medium
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.date: 10/30/2024
ms.reviewer: gusing
manager: frankbu
appliesto:
- Windows 10
- Windows 11
---

# Optimize video conferencing on Surface devices

Surface devices are designed to support seamless productivity across multiple workloads, including video conferencing—a critical component in today’s hybrid work environment. While Surface devices deliver exceptional performance for most tasks, optimizing video conferencing applications like Microsoft Teams ensures the best possible experience. The following recommendations help you enhance video quality, system responsiveness, and power efficiency during video calls.

## Surface drivers and firmware

Microsoft consistently releases updates for Surface devices, improving video conferencing and other collaborative workloads, especially in hybrid work environments. Key updates include:

- **System performance enhancements**: Improve device responsiveness during video conferencing.
- **Camera driver optimizations**: Reduce power consumption and enhance video quality, particularly in low-light conditions.
- **Graphics driver updates**: Boost visual clarity and processing efficiency during video calls and presentations.
- **Power settings optimizations**: Maintain consistent performance during video conferencing on AC power.

### Get updates to all devices

Make sure your organization has a reliable process for delivering these updates to all devices. If you use **Windows Update** or [Windows Update for Business](/windows/deployment/update/waas-manage-updates-wufb), your devices automatically receive the latest Surface updates upon release. Check for updates through Windows Update to verify that the newest drivers and firmware are installed. For more information, see:

- [Surface update history](https://www.microsoft.com/surface/support/install-update-activate/surface-update-history)  
- [Install Surface and Windows updates](https://www.microsoft.com/surface/support/performance-and-maintenance/install-software-updates-for-surface?)

If your organization uses tools like **Microsoft Intune** or **Configuration Manager** to install Surface drivers and firmware updates, review the following guidance: 

- [Download drivers and firmware for Surface](https://support.microsoft.com/help/4023482)  
- [Manage and deploy Surface driver and firmware updates](manage-surface-driver-and-firmware-updates.md)  
- [How to manage Surface driver updates in Configuration Manager](https://support.microsoft.com/help/4098906)

### Graphics driver updates for optimal video conferencing performance

Keeping graphics drivers up to date is essential for optimal video conferencing performance, especially when using applications like Microsoft Teams.

To ensure these improvements are applied:

- Use the latest version of **Microsoft Teams** to benefit from recent performance enhancements.
- Install the latest **graphics drivers** available for your device via **Windows Update** or your IT management tool (such as **Intune** or **Configuration Manager**).

For specific driver and firmware versions, see [Download drivers and firmware for Surface](https://support.microsoft.com/help/4023482).

### Power settings optimizations

Surface devices optimize performance for video conferencing applications, such as Microsoft Teams, using **Windows performance power settings**. On **Windows 11**, these settings are adjusted through **power mode**, while on **Windows 10**, they're accessible via the **performance power slider**.

Many Surface devices now include updates with power setting optimizations specifically targeting video conferencing workloads. However, to fully utilize these optimizations, especially for resource-intensive workloads, follow these recommendations:

1. **Connect the device to AC power** (power optimizations are limited on battery).  
2. **Adjust power mode or the performance slider** to **Better Performance** or **Best Performance** to enhance video conferencing quality.

Using **Windows Update** or **Windows Update for Business** ensures that the latest power optimizations are applied automatically.

## Learn more

- [Maximize your Surface battery life](https://support.microsoft.com/surface/maximize-your-surface-battery-life-45479867-a7fa-33dd-fc4d-6762e9b3b11a)
