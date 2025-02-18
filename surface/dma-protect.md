---
title: Direct Memory Access (DMA) protection on Surface devices
description: Learn how DMA protection enhances security on Surface devices by mitigating vulnerabilities related to removable SSDs and external storage.
ms.service: surface
ms.localizationpriority: medium
author: coveminer
ms.author: chauncel
ms.topic: overview
ms.date: 02/17/2025
ms.reviewer: carlol
manager: frankbu
appliesto:
- Windows 10
- Windows 11
---

# Direct Memory Access (DMA) protection on Surface devices

Direct Memory Access (DMA) protection is a security feature designed to safeguard Surface devices against unauthorized access via removable SSDs and external storage devices. By blocking unauthorized memory access from peripherals, DMA protection helps prevent **cold boot attacks**, **data exfiltration**, and other security risks.

## How DMA protection works

DMA protection ensures that only trusted and authorized devices can access system memory. It is particularly effective against attacks where malicious peripherals attempt to gain direct access to sensitive data.

On Surface devices, DMA protection:

- **Prevents unauthorized DMA access** from external devices connected via Thunderbolt, USB, or PCIe.
- **Triggers a shutdown and memory wipe** if tampering is detected in the removable SSD.
- **Works alongside other security measures** like **BitLocker, Secure Boot,** and **Windows Defender System Guard** to provide comprehensive protection.

## Supported Surface devices

DMA protection is **enabled by default** on newer Surface for Business devices, including:

- Surface Laptop 7th Edition, Qualcomm processor
- Surface Laptop 7th Edition, Intel processor  
- Surface Laptop 6  
- Surface Laptop 5  
- Surface Laptop 4  
- Surface Laptop 3  
- Surface Laptop SE  
- Surface Laptop Studio 2  
- Surface Laptop Studio  
- Surface Laptop Go 3  
- Surface Pro 11th Edition, Qualcomm processor  
- Surface Pro 11th Edition, Intel processor  
- Surface Pro 10  
- Surface Pro 10 with 5G  
- Surface Pro 9  
- Surface Pro 9 with 5G  
- Surface Pro 8  
- Surface Pro 7+  
- Surface Pro 7  
- Surface Pro X  
- Surface Go 4  
- Surface Go 3  

## How to check if DMA protection is enabled

To verify if **Kernel DMA protection** is enabled on your Surface device:

### Method 1: Using System Information (msinfo32)

1. Select **Start**, type `msinfo32.exe`, and press **Enter**.  
2. In the **System Information** window, scroll down to find **Kernel DMA Protection**.  
3. If the value is **Enabled**, DMA protection is active on your device.  

![System Information showing DMA protection enabled.](images/systeminfodma.png)

### Method 2: Using PowerShell

For IT admins managing multiple devices, PowerShell can provide quick verification:

```powershell
Get-ComputerInfo | Select-Object -Property DeviceGuard*
```

This command displays details about security policies, including DMA protection.
