---
title: Miracast on existing wireless network or LAN
description: Use Miracast over LAN or secure Wi-Fi to wirelessly project and interact with content on Surface Hub without extra hardware or setup. 
ms.service: surface-hub
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.date: 03/31/2025
ms.reviewer: 
manager: frankbu
ms.localizationpriority: medium
appliesto:
- Surface Hub
- Surface Hub 2S
---

# Miracast on existing wireless network or LAN

Miracast on your wireless network or LAN offers many benefits:

- Windows automatically detects when sending the video stream over this path is applicable.
- Windows will only choose this route if the connection is over Ethernet or a secure Wi-Fi network.
- Users don't have to change how they connect to a Miracast receiver. They use the same UX as standard Miracast connections.
- No changes to current wireless drivers or PC hardware are required.
- It works well with older wireless hardware not optimized for Miracast over Wi-Fi Direct.
- It uses an existing connection, which reduces the time to connect and provides a stable stream.

---

## Miracast support on Surface Hub 3

Microsoft [announced in January 2025](https://techcommunity.microsoft.com/blog/SurfaceITPro/introducing-edge-and-miracast-on-surface-hub-3/4365746) that for the first time ever, Teams Rooms on Windows – including Surface Hub 3 – will add support for Miracast wireless projection. Beyond simply sharing content, Miracast will also enable you to interact with the content on the Hub 3 display, with touch and pen input translated back to your PC. Surface Hub 3 will be able to desktop share Miracast-projected content into Teams meetings. Together with wired content sharing from PCs via center-of-table consoles (see next section), as well as Teams Cast and desktop sharing from PC over a Teams meeting, customers will now have an even more versatile and flexible set of options for sharing and collaborating on content with Surface Hub. Miracast support is committed; stay tuned for updates on availability timing.

---

## How it works

Users attempt to connect to a Miracast receiver through their Wi-Fi adapter. When the list of Miracast receivers is populated, Windows identifies that the receiver can support a connection over the infrastructure. When the user selects a Miracast receiver, Windows attempts to resolve the device's hostname via standard DNS and multicast DNS (mDNS). If the name isn't resolvable via either DNS method, Windows returns to establishing the Miracast session using the standard Wi-Fi direct connection.

> [!TIP]
> For more information on the connection negotiation sequence, see [Miracast over Infrastructure Connection Establishment Protocol (MS-MICE)](/openspecs/windows_protocols/ms-mice/9598ca72-d937-466c-95f6-70401bb10bdb?redirectedfrom=MSDN)

## Enabling Miracast over Infrastructure

You automatically have this feature if you have a Surface Hub or other Windows 10/11 device. To take advantage of it in your environment, you need to ensure the following is true within your deployment:

- Open TCP port: **7250**.
- A Surface Hub or Windows PC can act as a Miracast over Infrastructure *receiver*. A Windows PC or phone can act as a Miracast over Infrastructure *source*.
  - As a Miracast receiver, the Surface Hub or device must be connected to your enterprise network via Ethernet or a secure Wi-Fi connection (for example, using WPA2-PSK or WPA2-Enterprise security). If the Surface Hub or device is connected to an open Wi-Fi connection, Miracast over Infrastructure will disable itself.
    - As a Miracast source, the Windows PC or phone must be connected to the same enterprise network via Ethernet or a secure Wi-Fi connection.
- The DNS Hostname (device name) of the Surface Hub or device must be resolvable via your DNS servers. You can achieve this by allowing your Surface Hub to register automatically via Dynamic DNS or manually creating an A or AAAA record for the Surface Hub's hostname.
- Windows 10 PCs must be connected to the same enterprise network via Ethernet or a secure Wi-Fi connection.

It's important to note that Miracast over Infrastructure isn't a replacement for standard Miracast. Instead, the functionality is complementary, and provides an advantage to users who are part of the enterprise network. Users who are guests to a particular location and don’t have access to the enterprise network will continue to connect using the Wi-Fi Direct connection method.

The **InBoxApps/WirelessProjection/PinRequired** setting in the [SurfaceHub configuration service provider (CSP)](/windows/client-management/mdm/surfacehub-csp) isn't required for Miracast over Infrastructure. This is because Miracast over Infrastructure only works when both devices are connected to the same enterprise network. This removes the security restriction that was previously missing from Miracast. We recommend that you continue using this setting (if you used it previously) as Miracast will fall back to regular Miracast if the infrastructure connection doesn't work.

## Learn more

- [Troubleshoot display projection to Surface Hub](miracast-troubleshooting.md)
