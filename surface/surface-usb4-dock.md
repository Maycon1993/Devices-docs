---
title: Surface USB4 Dock overview
description:  Surface USB4 Dock - connect peripherals, get ultra-fast USB4 speeds, dual 4K monitors, 65-W power delivery in a compact, sustainable design.
ms.service: surface
ms.localizationpriority: medium
author: coveminer
ms.author: chauncel
ms.topic: overview
ms.date: 02/14/2025
ms.reviewer: angpatel
manager: frankbu
appliesto:
- Windows 10
- Windows 11
---

# Surface USB4 Dock overview

Surface USB4 Dock is a full stationary docking solution, with a compact, sleek design that keeps your desktop organized. The Surface USB4 Dock enables you to connect and power devices and accessories with 65-watt power delivery, ensuring peak performance throughout the workday.

- **Ultra-fast connectivity**: Get 40-Gbps data transfer via USB4, four times faster than USB 3.2.
- **Power delivery**: Includes a 100-W power supply delivering 65-W passthrough charging for laptops and accessory charging.
- **Dual screen support**: Supports up to two 4K monitors with HDMI or USB-C output, enhancing multitasking. Plus, single 8K monitor support at 30 HZ via USB-C.
- **Reliable Ethernet connectivity**: Supports Gigabit Ethernet, ensuring fast and reliable network connections.
- **Core commercial manageability features**: Equipped with essential capabilities such as PXE boot,[<sup>1</sup>](#references) WMI, and Media Access Control (MAC) address passthrough[<sup>2</sup>](#references)  for streamlined IT operations.
- **Universal compatibility**: Designed to work with Surface devices[<sup>3</sup>](#references) and compatible with numerous USB-C, USB4, and Thunderbolt 4 devices.
- **Compact and lightweight**: At 206 grams (7.2 ounces), USB4 Dock includes tactile indicators for easier port wayfinding.
- **Designed with sustainability in mind:** Contains more recycled materials than any previous Surface Dock, including 100% recycled tin, 100% recycled gold, and 50% recycled plastics.[<sup>4</sup>](#references) 


:::image type="content" source="images/surface-usb4-dock.png" alt-text="Screenshot of USB4 Dock.":::

---

## Manageability & security

Surface USB4 Dock comes with the following management and security features:

- **Firmware updates through Windows Update**: Keep your dock up to date with automatic updates  or downloadable driver and firmware packs.
- **MAC address passthrough**: Maintain consistent network identity across different docks for easy management in shared workspaces.[<sup>2</sup>](#references)
- **Wake-on-LAN (WOL)[<sup>5</sup>](#references) from Modern Standby**: IT admins can remotely wake devices connected to Surface USB4 Dock and automate management tasks.
  - Surface USB4 Dock doesn't support WOL with device-targeted MAC address passthrough. 
  - Alternative WOL pathways include using connected standby (Modern Standby) instead of WOL from S4/S5, or configuring the dock for MAC address passthrough rather than the device MAC address.  
- **PXE Boot:** IT admins can deploy operating systems, troubleshoot, and manage large numbers of devices in a network.[<sup>1</sup>](#references) 
- **Windows Management Instrumentation (WMI)**: IT admins can remotely monitor and manage the latest firmware, policy settings, and related data across Surface USB4 Dock and other Surface docks. For details, see [Manage Surface Dock with WMI](surface-dock-wmi.md).
- **Centralized support and warranty service**: IT admins can access direct support from the [Surface Management Portal](surface-management-portal.md) or [Surface Support Portal](surface-support-portal.md).

---

## Compatibility

Surface USB4 Dock is optimized for numerous USB-C/USB4/Thunderbolt 4-enabled devices,[<sup>3</sup>](#references) including the following Surface devices:

- Surface Laptop 7th Edition, Intel processor
- Surface Pro 11th Edition, Intel processor
- Surface Laptop 7th Edition, Snapdragon processor
- Surface Pro 11th Edition, Snapdragon processor
- Surface Pro 10
- Surface Laptop 6
- Surface Pro 9 (Intel/Wi-Fi)
- Surface Pro 8

Surface USB4 Dock is compatible with the following Surface for Business devices with USB-C[<sup>3</sup>](#references) ports:

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
> USB-C connection supports **one external display up to 4K at 60Hz** (when supported by device and display). Or you can [daisy chain more monitors](#daisy-chain-more-monitors).

> [!TIP]
> You can use Surface USB4 Dock with any host PC with USB4/ Thunderbolt 4. Full support for enterprise management and security features is exclusive to Surface devices. Automatic firmware updates via Windows Update only work on Windows-based PCs.

---

## Connections

Surface USB4 Dock is equipped with versatile ports to support modern workflows:

- **One front-facing USB-A** (USB 3.2 Gen 2, 7.5 W)
- **One front-facing USB-C** (USB4 Gen 3, compatible with Thunderbolt 4, video enabled, 7.5 W)
- **One rear-facing USB-C** (USB4 Gen 3, compatible with Thunderbolt 4, video enabled, 7.5 W)
- **One rear-facing HDMI 2.1**
- **One rear-facing USB-C for PSU only**
- **One Ethernet port** (1 Gbps)
- **Security lock support** (Kensington compatible)

---

## Sustainability

Microsoft’s commitment to sustainability is reflected in Surface USB4 Dock:

- **Recycled materials**: Contains a minimum of 55.2% recycled content. Surface USB4 Dock contains more recycled materials than any previous Surface dock, including 100% recycled tin, 100% recycled gold, and 50% recycled plastic.[<sup>4</sup>](#references) 
- **Thoughtful packaging:** 77% recycled content in wood-based fiber commercial packaging. 
- **Carbon-free electricity**: To meet Microsoft’s goal of 100% carbon-free electricity by 2030, 40% of our key devices suppliers transitioned to CFE in 2024.
- **Electric vehicle delivery**: In 2024, we expanded truckload electric vehicle capabilities to cover both of our United States distribution centers, enabling full truckloads within a 100-mile range of the distribution centers to be delivered via EV.
- **Sustainability goals**: Supporting Microsoft’s pledge to be carbon negative, water positive, and achieve zero waste by 2030. Learn more about [Microsoft Surface Sustainability](https://www.microsoft.com/corporate-responsibility/sustainability/).

---

## Compare Surface docks

| Feature                   | Surface USB4 Dock           | Surface Thunderbolt 4 Dock | Surface USB-C Travel Hub | Surface Dock 2          |
|---------------------------|--------------------------|-----------------------------|--------------------------|-------------------------|
| Type                      | Full stationary dock          | Most fully featured dock          | Portable hub            | Legacy dock    |
| Manageability features    | PXE boot,[<sup>1</sup>](#references) WMI, Wake-on-LAN[<sup>5</sup>](#references) | PXE boot, SEMM, WMI         | None                    | SEMM, WMI, Centralized Updates |
| Host connection           | USB-C/USB4           | USB-C/USB4              | USB-C                 | Surface Connect         |
| USB-A ports               | 1                      | 3                           | 1                       | 2                       |
| USB-C ports               | 2                        | 3                           | 1                       | 2                       |
| HDMI                      | 1                        | None                        | 1                       | None                   |
| Ethernet                  | 1 Gbps                   | 2.5 Gbps                    | 1 Gbps                   | 1 Gbps                  |
| Power passthrough         | 65 W                     | 96 W                         | None                    | 199 W                   |
| Monitor support           | Dual 4K @ 60 Hz          | Dual 4K @ 60 Hz              | Single monitor          | Dual 4K @ 60 Hz         |
| Designed for              | USB-C/USB4 devices      | Performance USB-C devices   | Universal USB-C devices | Surface devices w/ Connect |
| Manageability Features      |
| Wake-on-LAN[<sup>5</sup>](#references)  from Modern Standby | Yes                  | Yes                        | No                       | Yes                  |
| Wake-on-Power | Yes                  | Yes                        | No                       | Yes                  |
| Wake-on-LAN from S4/S5 sleep modes | No                | Yes                        | No                       | No                   |
| Network PXE boot[<sup>1</sup>](#references)              | Yes                  | Yes                        | Yes                      | Yes                  |
| SEMM host access control      | No                   | Yes                        | No                       | No                   |
| SEMM port access control      | No                   | Yes                        | No                       | No                   |
| Servicing support             | Windows Update, Surface App, or MSI | Windows Update, Surface App, or MSI | Windows Update or MSI | MSI                  |


## Connect multiple monitors to devices 

Surface USB4 Dock supports two 4K monitors at 60Hz via USB-C or HDMI 2.1 ports, or a single 8K monitor at 30Hz when connected over USB-C. Surface USB4 Dock  allows you to expand your visual workspace while working simultaneously on three screens. For dual 4K Monitor support you require a device with USB4/Thunderbolt 4 port and a supported device and display.

### Daisy chain more monitors

You can daisy chain up to eight monitors by connecting a series of display devices with a wired connection from monitor to monitor in a series. Don't connect each monitor directly to Surface USB4 Dock.

To daisy chain monitors, you need two or more monitors that support at least **DisplayPort 1.2** and **Multi-Stream Transport (MST).** Displays that function as a middle link in the chain must include **DisplayPort** output ports and input ports. You also need a video or graphics card (GPU) on your PC that supports **DisplayPort 1.2** and **MST.**

> [!NOTE]
> Resolution and refresh rate are reduced when daisy chaining two or more monitors.

**To connect your PC to multiple monitors using DisplayPort MST:**

1. Connect your PC to the **DisplayPort-In** connection on the first monitor.
2. Connect the **DisplayPort-Out** connection on the first monitor to the **DisplayPort-In** connection on the second monitor. To daisy chain more than two monitors, follow a similar sequence: The first monitor connects to the second, the second monitor connects to the third, and so on.
3. Use the On-Screen Display (OSD) menu. To enable **DisplayPort 1.2**, refer to your monitor's user manual. 

## Place an order

- [Surface USB4 Dock](https://www.microsoft.com/en-us/store/b/business-accessories?icid=CNav_BusinessStore_Surface)

## Appendix: Surface USB4 Dock Tech specs

| Dimensions                         | 4.72" x 2.36" x 0.59" (120 mm x 60 mm x 15 mm)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Weight                             | 206 g                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Connections                        | - 100-W power supply (up to 65-W passthrough). 100-W PSU included (not sold separately).<br>- USB-C /USB4 left-oriented Cable (80 cm) with dual LED indicator lights that confirm your Surface is docked and charging.<br>- USB4 supports: Charging, Dual display, up to 40 Gb/s data transfer. <br>- One front-facing USB-A (USB 3.2 Gen 2, 7.5 W)<br>- One front-facing USB-C (USB4 Gen 3, compatible with Thunderbolt 4, video display enabled, 7.5 W)<br>- One rear-facing USB-C (USB4 Gen 3, compatible with Thunderbolt 4, video display enabled, 7.5 W)<br>- One rear facing HDMI 2.1.<br>- One rear-facing USB-C for PSU only.<br>- One Ethernet (1 Gbit/s)<br>- Security lock support (Kensington compatible)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| What’s in the box                  | - Microsoft Surface USB4 Dock<br>- 100 W USB-C Power Supply                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Manageability (Commercial only)    | For supported host devices:<br><br>- Media Access Control (MAC) address passthrough[<sup>2</sup>](#references)<br>- Firmware update through Windows Update and Surface app<br>- Wake on LAN from Modern Standby                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Accessibility                      | Tactile indicators for easily identifying the ports                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Sustainability                     | Surface USB4 Dock is designed with sustainability in mind<br><br>**Sustainability in the supply chain**<br>- Our supply chain for devices is shifting to 100% carbon-free electricity for Microsoft-related production.<br>- At least 89 key device suppliers transitioned to carbon-free electricity with more in progress.<br> - To meet our goal of 100% carbon-free electricity by 2030, 40% of key device suppliers transitioned to CFE in 2024, expanding CFE use to 392 K MWh and avoiding 232 K mtCO2e in emissions.<br><br>**Electric Vehicle delivery**<br>- In 2024, we expanded truckload electric vehicle capabilities to cover both of our United States distribution centers.<br><br>**More recycled materials**<br>- Surface USB4 Dock contains more recycled materials than any previous Surface dock, including 100% recycled tin, 100% recycled gold, and 50% recycled plastic.[<sup>4</sup>](#references)<br><br>Microsoft set a goal to be carbon negative, water positive, and achieve zero waste by 2030. Learn more about how we design with sustainability in mind [Microsoft Surface Sustainability](https://www.microsoft.com/en-us/corporate-responsibility/sustainability/) |
| Warranty[<sup>7</sup>](#references)                  | One-year limited warranty                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |


### References

1. Network PXE boot requires the latest UEFI update on host devices, currently available for Intel-based devices, with a subsequent update planned for Arm-based devices. To learn more, see [How to use Surface UEFI - Microsoft Support](https://support.microsoft.com/surface/how-to-use-surface-uefi-df2c8942-dfa0-859d-4394-95f45eb1c3f9).
2. MAC address passthrough is available on the following host devices: Surface Go 4, Surface Laptop Go 3, Surface Laptop Studio 2, Surface Laptop 6 for Business, Surface Pro 10 for Business, Surface Pro 11th Edition (Snapdragon and Intel processors), Surface Laptop 7th Edition (Snapdragon and Intel processors), Surface Pro 11th Edition 5G, and Surface Pro 10 with 5G.
3. Surface USB4 Dock is compatible with Surface devices that support USB-C charging (devices later than Surface Pro 7 and Surface Laptop 3). To learn more, see [USB-C and Fast Charging for Surface - Microsoft Support](https://support.microsoft.com/surface/usb-c-and-fast-charging-for-surface-d320ab19-e4ed-c36d-7458-7d7aec69d34a).
4. Surface USB4 Dock, excluding power supply, contains 55.2% recycled content. This includes 11.8% recycled plastics, consisting of a minimum of 50% recycled plastics and 0.3% other recycled metals, consisting of 100% recycled gold in PCB and 100% recycled tin in solder. Based on validation performed by Underwriter Laboratories, Inc. using Environmental Claim Validation Procedure (EVCP) for Recycled Content, UL EVCP-2809-2, Second Edition, dated June 20, 2024. Recycled Content is defined in accordance with ISO 14201.
5. To support Wake-on-LAN, Surface devices must be plugged into AC power and use a Surface Ethernet adapter or docking device that is connected to a wired network.
6. Surface USB4 Dock is compatible with USB-C devices. However, when connected, it operates at the speeds and capabilities of the USB-C port. USB-C/USB 3.2 connection supports one external display up to 4K at 60 Hz (when supported by device and display). Or you can daisy chain more monitors, as described on this page.
7. Microsoft’s Limited Warranty is in addition to your consumer law rights. 

