---
title: Connect devices to Surface Hub 2S
description: Connect devices to Surface Hub 2S with USB-C, HDMI, or Bluetooth. 
ms.service: surface-hub
author: coveminer
ms.author: chauncel
manager: frankbu
ms.topic: how-to
ms.date: 11/07/2024
ms.localizationpriority: Medium
appliesto:
- Surface Hub 2S

---

# Connect devices to Surface Hub 2S

[!INCLUDE [Hub 2S EoS](includes/hub2s-eos.md)]

Surface Hub 2S supports flexible device connectivity for seamless collaboration and content sharing. You can connect external devices, mirror displays, and use third-party peripherals like video conference cameras, conference phones, and room system devices. Surface Hub 2S enables interactive controls through TouchBack and InkBack, enhancing collaboration during meetings.

## Connection options and configurations

### Connect via cables

To project content with cables, connect using the ports along the bottom edge of the compute cartridge. Available ports include HDMI, USB-C, USB-A, Ethernet, and DisplayPort.

- **HDMI and USB-C** – Connect for audio and video input. USB-C supports TouchBack and InkBack, allowing control from Surface Hub 2S.
- **DisplayPort** – Use DisplayPort to mirror Surface Hub’s display to another screen.

> [!Important]
> Surface Hub 2S uses the selected video input until a new connection is made, the connection is disrupted, or the Connect app is closed.

> [!NOTE]
> Surface Hub 2S uses the video input selected until a new connection is made, the existing connection is disrupted, or the Connect app is closed.

## Project using cables to Surface Hub 2S

To project your screen with cables, connect using the ports along the bottom edge of the compute cartridge. The compute cartridge has an HDMI port, a USB-C port, USB-A, and the Ethernet port and DisplayPort.

You can project in with USB-C or HDMI—the DisplayPort is only for mirroring your Surface Hub’s screen on another screen.

:::image type="content" source="images/computer-cartridge-ports.png" alt-text="Screenshot of the compute cartridge that has an HDMI port, a USB-C port, USB-A, as well as the Ethernet port and DisplayPort.":::

### Recommended wired configurations for Surface Hub 2S

For optimal video and interactive functionality, use native cable connections where possible (e.g., USB-C to USB-C or HDMI to HDMI). Alternative connections like MiniDP to HDMI or MiniDP to USB-C will work, though extra configuration may be required. 

> [!NOTE]
> This section only applies to Surface Hub 2S running Windows 10 Team edition. 


| Connection     | Functionality                      | Description                                                                                        |
| ------------------ | ----------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **HDMI + USB-C**   | HDMI for audio/video<br>USB-C for TouchBack/InkBack | HDMI provides audio/video while USB-C supports TouchBack and InkBack. Connect HDMI first for best results. |
| **USB-C**          | Audio/video<br>TouchBack/InkBack          | Single cable provides audio, video, and TouchBack/InkBack. HDCP is enabled.                               |
| **HDMI (in port)** | Audio/video                               | Single cable for audio and video. TouchBack/InkBack not supported. HDCP is enabled.                       |
| **MiniDP 1.2 out** | Video-out for display mirroring           | Mirrors Surface Hub 2S display on a larger screen. 

When connecting a guest computer via USB-C, Surface Hub 2S automatically configures several USB devices to enable TouchBack and InkBack, as shown in the Device Manager table below.


|Peripheral| Listing in Device Manager |
| ---------------------------- |------------- |
| Human interface devices | HID-compliant consumer control device<br>HID-compliant pen<br>HID-compliant pen (duplicate item)<br>HID-compliant pen (duplicate item)<br>HID-compliant touch screen<br>USB Input Device<br>USB Input Device (duplicate item) |
| Keyboards | Standard PS/2 keyboard |
| Mice and other pointing devices | HID-compliant mouse |
| USB controllers | Generic USB hub<br>USB composite device |

## Connect video-in to Surface Hub 2S

You can input video to Surface Hub 2S through USB-C or HDMI. Supported resolutions and frame rates vary by signal type. 

### Surface Hub 2S video-in settings

| Signal Type | Resolution | Frame rate | HDMI | USB-C |
| --------------- | -------------- | -------------- | -------- | --------- |
| PC              | 640 x 480      | 60             | ✔       | ✔         |
| PC              | 720 x 480      | 60             | ✔       | ✔         |
| PC              | 1024 x 768     | 60             | ✔       | ✔         |
| PC              | 1280 x 720     | 60             | ✔       | ✔         |
| PC              | 1600 x 900     | 60             | ✔       | ✔         |
| PC              | 1920 x 1080    | 60             | ✔       | ✔         |
| PC              | 3840 x 2560    | 30             | ✔       | ✔         |
| HDTV            | 480p           | 60             | ✔       | ✔         |
| HDTV            | 720p           | 60             | ✔       | ✔         |
| HDTV            | 1080p          | 60             | ✔       | ✔         |
| 4K UHD          | 3840 x 2560    | 30             | ✔       | ✔         |

> [!NOTE]
> The 4K UHD resolution is only supported on compute module ports. Video from an external PC may appear smaller on Surface Hub 2S.

## Mirror Surface Hub 2S display on another device

You can output video to another display using MiniDP, as indicated in the following table.

### Surface Hub 2S video-out settings

Surface Hub 2S includes a MiniDP video-out port, allowing you to project visual content to another display. If you plan to use Surface Hub 2S to project to an external screen, follow these guidelines for optimal results.

| **Signal Type** | **Resolution** | **Frame rate** | **MiniDP** |
| --------------- | -------------- | -------------- | ---------- |
| PC              | 640 x 480      | 60             | ✔         |
| PC              | 720 x 480      | 60             | ✔         |
| PC              | 1024 x 768     | 60             | ✔         |
| PC              | 1920 x 1080    | 60             | ✔         |
| PC              | 3840 x 2560    | 60             | ✔         |
| HDTV            | 720p           | 60             | ✔         |
| HDTV            | 1080p          | 60             | ✔         |
| 4K UHD          | 3840 x 2560    | 60             | ✔         |

#### Recommendations for projecting to another display

- **Keyboard required:** Before you begin, connect an external keyboard to Surface Hub 2S, either wired or Bluetooth-enabled. Unlike the original Surface Hub, Surface Hub 2S does not include a keyboard in the shipping package.
  
- **Set to duplicate mode:** Surface Hub 2S supports video-out in duplicate mode only. To configure this setting:
  1. Press **Windows logo key** + **P** to open the Project pane on the right side of the screen, then select **Duplicate**.
  2. After your session, select **End Session** to save the duplicate setting for future use.
  
- **Aspect ratio considerations:** Surface Hub 2S has a 3:2 display aspect ratio, which may differ from the aspect ratio of the external display. When projecting, the MiniDP output will maintain the 3:2 ratio, which may result in letterboxing or curtaining on screens with other aspect ratios, like 16:9.

> [!TIP]
> If projecting to a 16:9 monitor, black bars may appear on the left and right sides of the display. This is normal and does not require adjustments to the second display.## Select cables

Use these recommendations for cables:

- **USB** – USB 3.1 Gen 2 cables for optimal performance.
- **MiniDP** – Certified DisplayPort cables up to 3 meters.
- **HDMI** – For long-distance connections, HDMI cables are recommended. Install repeaters if necessary.

> [!TIP]
> Most DisplayPort sources automatically switch to HDMI if detected.

## Connect wirelessly to Surface Hub 2S

Surface Hub 2S supports wireless connections via Miracast on Windows 10 and 11 devices.

1. Press **Windows logo key** + **K**.
2. Select Surface Hub 2S from the list of nearby devices.
3. Enter a PIN if prompted by your administrator.

> [!NOTE]
> If Surface Hub 2S doesn’t appear, sign in directly to end any previous session before reconnecting.
### Enable device control from Surface Hub

When a Windows 8 or later device is connected, select **Allow mouse, keyboard, touch, and pen input** on the connected device to control it from Surface Hub 2S. If using HDMI, add a USB cable to enable interactive input.

## Connect peripherals to Surface Hub 2S

### Bluetooth accessories

You can connect Bluetooth accessories, including mice, keyboards, headsets, speakers, and Surface Hub 2S pens. 

> [!TIP]
> After pairing a Bluetooth audio device, update microphone and speaker settings as needed. For more details, see [Local management for Surface Hub settings](local-management-surface-hub-settings.md).

