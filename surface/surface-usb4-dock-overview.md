---
title: Surface USB4 Dock technical overview
description:  Surface USB4 Dock - connect peripherals, get ultra-fast USB4 speeds, dual 4K monitors, 65-W power delivery in a compact, sustainable design.
ms.service: surface
ms.localizationpriority: medium
author: coveminer
ms.author: chauncel
ms.topic: overview
ms.date: 01/30/2025
ms.reviewer: angpatel
manager: frankbu
appliesto:
- Windows 10
- Windows 11
---

# Surface USB4 Dock technical overview

Surface USB4 Dock is a full stationary docking solution, with a compact, sleek design that keeps your desktop organized. The Surface USB4 Dock enables you to connect and power devices and accessories with 65-watt power delivery, ensuring peak performance throughout the workday.

- **Ultra-fast connectivity**: Get 40Gbps data transfer via USB4®, four times faster than USB 3.2.
- **Power delivery**: Includes a 100W power supply delivering 65W passthrough charging for laptops and accessory charging.
- **Dual screen support**: Supports up to two 4K monitors with HDMI or USB-C® output, enhancing multitasking. Plus, single 8K monitor support at 30 HZ via USB-C.
- **Reliable Ethernet connectivity**: Supports Gigabit Ethernet, ensuring fast and reliable network connections.
- **Core commercial manageability features**: Equipped with essential capabilities such as PXE boot,[<sup>1</sup>](#references) WMI, and Mac Address Passthrough for streamlined IT operations.
- **Universal compatibility**: Designed to work with Surface devices[<sup>2</sup>](#references) and compatible with numerous USB-C®, USB4®, and Thunderbolt™ 4 devices.
- **Compact and lightweight**: At 206 grams (7.2 ounces), USB4 Dock includes tactile indicators for port wayfinding.
- **Designed with sustainability in mind:** - Made with more recycled materials than any previous Dock, including a minimum of 43.1% recycled content in the enclosure.



:::image type="content" source="images/surface-usb4-dock.png" alt-text="Screenshot of USB4 Dock Dock.":::

---

## Manageability and security

Surface USB4 Dock comes with the following management and security features:

- **Firmware updates through Windows Update**: Keep your dock up to date with automatic updates  or downloadable driver and firmware packs.
- **MAC address passthrough**: Maintain consistent network identity across different docks for easy management in shared workspaces.
- **Wake-on-LAN from Modern Standby**: IT admins can remotely wake devices connected to Surface USB4 Dock and automate management tasks.
  - Surface USB4 Dock does not currently support Wake-on-LAN with MAC address passthrough. 
  - Alternative pathways for Wake-on-LAN include using connected standby, instead of Wake-on-LAN from S4/S5, or targeting the dock for MAC address passthrough instead of the device.  
  - WOL is not available for in-market devices but is expected to be available in future firmware updates (targeted for April 2025).
- **PXE Boot:** IT admins can deploy operation systems, troubleshoot, and manage large numbers of devices in a network. 
  - PXE boot is currently available with IPv4 for all supported devices, including Surface Pro 11th Edition and Surface Laptop 7th Edition.
  - PXE Boot with IPv6 is supported for all in-market devices. Support for IPv6 on new devices, including Surface Pro 11th Edition and Surface Laptop 7th Edition, is planned for a Windows Update targeted for April 2025
- **Windows Management Instrumentation (WMI)**: IT admins can remotely monitor and manage the latest firmware, policy settings, and related data across Surface USB4 Dock and other Surface docks. For details, see [Manage Surface Dock with WMI](surface-dock-wmi.md).
- **Centralized support and warranty service**: IT admins can access direct support from the [Surface Management Portal](surface-management-portal.md) or [Surface Support Portal](surface-support-portal.md).

## Compatibility

Surface USB4 Dock is optimized for numerous USB-C/USB4/Thunderbolt™ 4-enabled devices, including the following Surface devices.

- Surface Laptop 7th Edition with Intel Core Ultra Processor (Series 2)
- Surface Pro 11th Edition with Intel Core Ultra Processor (Series 2)
- Surface Pro 11th Edition with Snapdragon X Elite or Plus Processor
- Surface Laptop 7th Edition with Snapdragon X Elite or Plus Processor
- Surface Pro 10
- Surface Laptop 6
- Surface Pro 9 (Intel/Wi-Fi)
- Surface Pro 8

Surface USB4 Dock is compatible with the following Surface for Business devices with USB-C[<sup>2</sup>](#references) ports:

- Surface Pro 7 and later
- Surface Pro X (all generations)
- Surface Laptop 3 and later
- Surface Laptop Studio (all generations)
- Surface Laptop Go (all generations)
- Surface Laptop SE
- Surface Go (all generations)
- Surface Book 2 and later

For a full list of compatible devices and details, refer to the [USB-C and Fast Charging for Surface](https://support.microsoft.com/surface/usb-c-and-fast-charging-for-surface-d320ab19-e4ed-c36d-7458-7d7aec69d34a) page.

> [!NOTE]
> USB-C connection supports **one external display up to 4K at 60Hz** (when supported by device and display). Or you can daisy chain more monitors. To learn more, see [Connect multiple monitors to devices](/surface/surface-dock-whats-new#connect-multiple-monitors-to-devices).

> [!TIP]
> You can use Surface USB4 Dock with any host PC with USB4/ Thunderbolt 4. Full support for enterprise management and security features is exclusive to Surface devices. Automatic firmware updates via Windows Update only work on Windows-based PCs.

---

## Connections

Surface USB4 Dock is equipped with versatile ports to support modern workflows:

- **One front-facing USB-A** (USB 3.2 Gen 2, 7.5W)
- **One front-facing USB-C** (USB4 Gen 3, compatible with Thunderbolt 4, video enabled, 7.5W)
- **One rear-facing USB-C** (USB4 Gen 3, compatible with Thunderbolt 4, video enabled, 7.5W)
- **One rear-facing HDMI 2.1**
- **One rear-facing USB-C for PSU only**
- **One Ethernet port** (1Gbps)
- **Security lock support** (Kensington compatible)

---

## Sustainability

Microsoft’s commitment to sustainability is reflected in Surface USB4 Dock:

- **Recycled materials**: Up to 90% recycled plastic in the enclosure.
- **Carbon-free electricity**: Supply chain shifts to 100% carbon-free electricity for Microsoft-related production.
- **Electric vehicle delivery**: Last-mile delivery utilizes electric vehicles where possible.
- **Sustainability goals**: Supporting Microsoft’s pledge to be carbon negative, water positive, and achieve zero waste by 2030. Learn more about [Microsoft Surface Sustainability](https://www.microsoft.com/corporate-responsibility/sustainability/).

---

## Compare Surface docks

| Feature                   | Surface USB4 Dock           | Surface Thunderbolt 4 Dock | Surface USB-C Travel Hub | Surface Dock 2          |
|---------------------------|--------------------------|-----------------------------|--------------------------|-------------------------|
| Type                      | Full stationary dock          | Most fully featured dock          | Portable hub            | Legacy dock    |
| Manageability features    | PXE boot, WMI, Wake-on-LAN | PXE boot, SEMM, WMI         | None                    | SEMM, WMI, Centralized Updates |
| Host connection           | USB-C/USB4           | USB-C/USB4              | USB-C                 | Surface Connect         |
| USB-A ports               | 1                      | 3                           | 1                       | 2                       |
| USB-C ports               | 2                        | 3                           | 1                       | 2                       |
| HDMI                      | 1                        | None                        | 1                       | None                   |
| Ethernet                  | 1Gbps                   | 2.5Gbps                    | 1Gbps                   | 1Gbps                  |
| Power passthrough         | 65W                     | 96W                         | None                    | 199W                   |
| Monitor support           | Dual 4K @ 60Hz          | Dual 4K @ 60Hz              | Single monitor          | Dual 4K @ 60Hz         |
| Designed for              | USB-C/USB4 devices      | Performance USB-C devices   | Universal USB-C devices | Surface devices w/ Connect |
| Manageability Features      |
| Wake-on-LAN from Modern Standby | Yes                  | Yes                        | No                       | Yes                  |
| Wake-on-LAN from S4/S5 sleep modes | ??                | Yes                        | No                       | No                   |
| Network PXE boot              | Yes                  | Yes                        | Yes                      | Yes                  |
| SEMM host access control      | No                   | Yes                        | No                       | No                   |
| SEMM port access control      | No                   | Yes                        | No                       | No                   |
| Servicing support             | Windows Update, Surface App, or MSI | Windows Update, Surface App, or MSI | Windows Update or MSI | MSI                  |


## Connect multiple monitors to devices 

Surface USB4 Dock supports up to two 4K monitors with HDMI or USB-C output, enhancing multitasking.  

You can daisy chain up to eight monitors by connecting a series of display devices using a wired connection from monitor to monitor in a series, rather than connecting each monitor directly to Surface USB4 Dock.

To daisy chain monitors, you need two or more monitors that support at least **DisplayPort 1.2** and **Multi-Stream Transport (MST).** Displays that function as a middle link in the chain must include **DisplayPort** output ports and input ports. You also need a video or graphics card (GPU) on your PC that supports **DisplayPort 1.2** and **MST.**

> [!NOTE]
> Resolution and refresh rate is reduced when daisy chaining two or more monitors.

**To connect your PC to multiple monitors using DisplayPort MST:**

1. Connect your PC to the **DisplayPort-In** connection on the first monitor.
2. Connect the **DisplayPort-Out** connection on the first monitor to the **DisplayPort-In** connection on the second monitor. To daisy chain more than two monitors, follow a similar sequence: The first monitor connects to the second, the second monitor connects to the third, and so on.
3. Use the On-Screen Display (OSD) menu, to enable **DisplayPort 1.2** on your monitor. To learn more, refer to the user manual of your monitor.

## Place an order

- [Surface USB4 Dock](https://www.microsoft.com/en-us/store/b/business-accessories?icid=CNav_BusinessStore_Surface)

## Appendix: Surface USB4 Dock Tech specs

| Dimensions                         | 4.72" x 2.36" x 0.59" (120mm x 60mm x 15mm)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Weight                             | 206 g                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Connections                        | 100-W power supply (up to 65-W passthrough). (100 PSU in-box not sold separately)<br>- USB-C /USB4 left-oriented Cable (80 cm) with dual LED indicator lights that confirm your Surface is docked and charging.<br>- USB4 supports: Charging, Dual display, up to 40Gb/s data transfer. <br>- 1 front-facing USB-A (USB 3.2 Gen 2, 7.5W)<br>- 1 front-facing USB-C (USB4 Gen 3, compatible with ThunderboltTM 4, video display enabled, 7.5W)<br>- 1 rear-facing USB-C (USB4 Gen 3, compatible with ThunderboltTM 4, video display enabled, 7.5W)<br>- 1 rear facing HDMITM 2.1.<br>- 1 rear-facing USB-C for PSU only.<br>- 1 Ethernet (1Gbit/s)<br>- Security lock support (Kensington compatible)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| What’s in the box                  | Microsoft Surface USB4 Dock<br>100 W USB-C Power Supply                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Manageability (Commercial only)    | For supported host devices:<br><br>- Media Access Control (MAC) address passthrough[<sup>3</sup>](#references)<br>- Firmware update through Windows Update and Surface app<br>- Wake on LAN from Modern Standby, S4/S5                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Accessibility                      | Tactile indicators for easily identifying the ports                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Sustainability                     | Surface USB4 Dock is designed with sustainability in mind<br><br>**Sustainability in the supply chain**<br>- Our supply chain for devices is shifting to 100% carbon-free electricity for Microsoft-related production<br><br>**Electric Vehicle delivery**<br>- To reduce our carbon emissions, we're investing in electric vehicles for the last mile delivery where possible.<br>- 25% of online orders in Europe were delivered with an electric or carbon neutral vehicle.<br>- Full truckloads within 100 miles of our Ontario, California, distribution center are made using electric vehicles<br><br>**More recycled materials**<br>- Up to ##% of Surface Reeves’ enclosure is made from 90% recycled plastic<br>- Made with more recycled materials than any previous Dock, including a minimum of 43.1% recycled content in the enclosure [<sup>4</sup>](#references)<br>- Surface USB4 Dock contains a minimum of ##% recycled content[<sup>5</sup>](#references)<br>- Surface USB4 Dock contains more recycled materials than any previous Dock, including recycled tin, recycled gold, and recycled plastic. <br>- <br><br>Microsoft set a goal to be carbon negative, water positive, and achieve zero waste by 2030. Learn more about how we design with sustainability in mind [Microsoft Surface Sustainability](https://www.microsoft.com/en-us/corporate-responsibility/sustainability/) |
| Warranty[<sup>6</sup>](#references)                  | 1-year limited warranty                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

### References

1. Network PXE boot requires the latest UEFI update on host devices., pending availability anticipated for MSD. To learn more, see How to use Surface UEFI - Microsoft Support.
1. Surface USB4 Dock is compatible with Surface devices that support USB-C charging (devices later than Surface Pro 7 and Surface Laptop 3). To learn more, see [USB-C and Fast Charging for Surface - Microsoft Support](https://support.microsoft.com/surface/usb-c-and-fast-charging-for-surface-d320ab19-e4ed-c36d-7458-7d7aec69d34a)
1. Surface USB4 Dock is compatible with USB-C devices. However, when connected, it operates at the speeds and capabilities of the USB-C port. USB-C/USB 3.2 connection supports 1 external display up to 4K at 60Hz (when supported by device and display). Or you can daisy chain more monitors, as described in the section on this page: Connect multiple monitors to devices without USB4/Thunderbolt 4
1. MAC address passthrough are available on select host devices and supported operating systems.
1. TBD
1. TBD
1. Microsoft’s Limited Warranty is in addition to your consumer law rights.
