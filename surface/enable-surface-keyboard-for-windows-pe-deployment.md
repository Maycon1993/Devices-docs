---
title: How to enable the Surface Laptop keyboard during MDT deployment 
description: Learn how to enable the Surface Laptop keyboard during MDT deployment by importing necessary drivers into the Windows PE environment.
ms.service: surface
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.reviewer: carlol
ms.localizationpriority: medium
manager: frankbu
ms.date: 04/14/2025
appliesto:
- Surface Laptop (all generations)
- Surface Laptop Studio (all generations)
- Surface Pro 8
- Surface Pro 9
- Surface Pro 10
- Windows 10
- Windows 11
---

# How to enable a Surface Laptop keyboard, Surface Pro Keyboard, or Surface Pro Type Cover during Windows deployment

This article provides information necessary to enable the keyboard and trackpad on some Surface devices when using a Windows deployment process like System Center Configuration Manager (SCCM) operating system deployment (OSD), or other deployment methodologies.   

> [!TIP]
> When using keyboard drivers for Surface Laptop 2 and Surface Laptop 3 in the same Windows PE boot instance, you might need to manually reset the firmware if the keyboard or touchpad don’t work in Windows PE:
>
> - Press and hold the Power button for 30 seconds. If you're connected to a power supply unit (PSU), press and hold the Power button until you see the light at the end of the PSU cord briefly turn off before turning back on.

> [!IMPORTANT]
> If you're deploying a Windows 10 image to a Surface Laptop that has Windows 10 in S mode preinstalled, see KB [4032347, Problems when deploying Windows to Surface devices with preinstalled Windows 10 in S mode](https://support.microsoft.com/help/4032347/surface-preinstall-windows10-s-mode-issues).

## Download and extract keyboard drivers

1. Download the latest Surface .msi file for your Surface device from the following page: [Manage & deploy Surface driver & firmware updates](manage-surface-driver-and-firmware-updates.md).

2. Extract the contents of the Surface .msi file to a folder that you can easily locate (for example, c:\surface_drivers). To extract the contents, open an elevated Command Prompt window and run the command from the following example:

   ```cmd
   Msiexec.exe /a SurfaceLaptop_Win10_15063_1703008_1.msi targetdir=c:\surface_drivers /qn
   ```

 > [!NOTE]
 > Check the extracted .msi package to determine the format and directory structure. The directory structure starts with either SurfacePlatformInstaller (older .msi files) or SurfaceUpdate (newer .msi files) depending on when the .msi file was released.

## Import drivers for Surface devices

Import the following folders as appropriate for your Surface device.You will need to import these drivers into Windows PE if you need to use the keyboard or trackpad during early parts of your OS deployment.  

| Device                           | Import folders        | More information  |
| ------------------------------- | ------------------------ | -----------------------|
| **Surface Laptop 7 (Intel)**            |           ---              |     Coming soon   |
| **Surface Laptop 6** | ialpss2gpio2mtl<br>ialpss2i2cmtl<br>ialpss2spimtl<br>ialpss2uart2mtl<br>intcpmt<br>intelquickspi<br>msu53cx22x64sta<br>msu56cx22x64sta<br>surfaceacpiplatformextension<br>surfacebattery<br>surfacebutton<br>surfacedockintegration<br>surfacehidminidriverwinre<br>surfacehotplug<br>surfaceintegrationdriver<br>surfacepanel<br>surfacepen217integration<br>surfacepenblelcaddradaptationdriver<br>surfaceserialhub<br>surfaceservicenulldriver<br>surfacesptclient<br>surfacetimealarmacpifilter<br>surfacetouchpenprocessor0c88update<br>surfacetouchpenprocessor0c89update<br>surfaceucmucsihidclient<br>tbtslimhostcontroller |If you're using a Windows 10 version of Windows PE and you need Surface Ethernet connectivity, you also need to import the folder “msump64x64sta” from the Windows 10 MSI.|
| **Surface Pro 11 (Intel)**           | ---  |Coming soon|
| **Surface Pro 10** | acpiplatformextension<br>Battery<br>DockIntegration<br>HidMini<br>HotPlug<br>ialpss2gpio2mtl<br>ialpss2i2cmtl<br>ialpss2spimtl<br>ialpss2uart2mtl<br>Integration<br>IntelQuickSPI<br>msu53cx22x64sta<br>msu56cx22x64sta<br>penwirelesschargerhotkey<br>SarManager<br>SerialHub<br>Service<br>SMFClient<br>smfdisplayclient<br>timealarmacpifilter<br>UcmUcsiHidClient|If you're using a Windows 10 version of Windows PE and you need Surface Ethernet connectivity, you also need to import the folder “msump64x64sta” from the Windows 10 MSI.|
| **Surface Pro 9 with Intel processor** | adlserial<br>alderlakepchpsystem<br>alderlakesystem<br>gna<br>intelprecisetouch<br>managementengine<br>msump64x64sta<br>surfaceacpiplatformextension<br>surfacebattery<br>surfacedockintegration<br>surfacehidmini<br>surfacehotplug<br>surfaceintegrationdriver<br>surfacesarmanager<br>surfaceserialhubdriver<br>surfaceservicenulldriver<br>surfacetimealarmacpifilter<br>surfaceucmucsihidclient<br>tbtslimhostcontroller |n/a |
| **Surface Laptop Studio 2**     | Adl-rplserialLPSS<br>cardreader<br>heci<br>intelquickspi<br>msu53cx22x64sta<br>realtekEthernet<br>surfaceacpiplatformextension<br>surfacebattery<br>surfacedockintegration<br>surfacehidminidriver<br>surfacehotplug<br>surfaceintegrationdriver<br>surfacepenwirelesschargerhotkey<br>surfacesarmanager<br>surfaceserialhub<br>surfacesptclient<br>surfacetimealarmacpifilter<br>surfaceucmucsihidclient<br>surfacewakeontouchcontrol<br>wotquickspiextensionport1 | n/a     |
| **Surface Laptop Studio**     | intelthcbase <br>managementengine <br>surfaceacpiplatformextension <br>surfacebattery <br>SurfaceEthernetAdapter <br>surfacehidmini  <br>surfacehotplug <br>surfaceintegration <br>surfacesar <br>surfaceserialhub <br>surfacesmfclient <br>surfacesmfdisplayclient <br>surfacesptclient <br>surfacetimealarmacpifilter <br>surfacevirtualfunctionenum <br>tbtslimhostcontroller <br>tglchipset <br>tglserial <br>   | n/a     |
| **Surface Pro 8**       | intelthcbase <br> ManagementEngine <br> surfaceacpiplatformextension <br> SurfaceBattery <br> SurfaceCoverClick <br> SurfaceEthernetAdapter <br> SurfaceHidMini <br> SurfaceHotPlug <br> surfaceintegrationdriver <br> SurfaceSar <br> SurfaceSerialHub <br> surfacetimealarmacpifilter <br> surfacetypecoverv7fprude <br> SurfaceUcmUcsiHidClient <br> surfacevirtualfunctionenum <br> tbtslimhostcontroller <br> TglChipset <br> TglSerial| n/a  |
| **Surface Laptop 5 with Intel processor**| adlserial <br> alderlakepchpsystem <br> gna <br> heci <br> intelprecisetouch <br> msump64x64sta <br> surfaceacpiplatformextensiondriver <br> surfacebattery <br> surfacebutton <br> surfacedockintegration <br> surfacehidminidriver <br> surfacehotplug <br> surfaceintegration <br> surfaceserialhubdriver <br> surfacetimealarmacpifilter <br> tbtslimhostcontroller      |  n/a |
| **Surface Laptop 4 with Intel processor** | TglSerial <br> IntelPreciseTouch <br> SurfaceEthernetAdapter <br> SurfaceBattery <br> SurfaceHidMini <br> SurfaceHotPlug <br> SurfaceSerialHub <br> SurfaceTconDriver <br> surfacetimealarmacpifilter <br> surfacevirtualfunctionenum <br> TglChipset <br> ManagementEngine          | n/a    |
| **Surface Laptop 4 with AMD processor**| U0361415 <br> AMDfendr <br> AMDGpio2 <br> AMDI2c <br> AMDLpcFilterDriverAMDMicroPEP <br> AMDPsp <br> AMDSmf <br> AMDSpi <br> AMDUart <br> SurfaceEthernetAdapter <br> SMBUS <br> SurfaceBattery <br> SurfaceButton <br> SurfaceDigitizerHidSpiExtnPackage <br> SurfaceHIDFriendlyNames <br> SurfaceHidMini <br> SurfaceHotPlug <br> SurfaceOemPanel <br> SurfacePowerMeter <br> SurfacePowerTrackerCore <br> SurfaceSerialHub <br> SurfaceSMFClient <br> SurfaceSmfDisplayClient <br> SurfaceSystemManagementFramework <br> SurfaceTconDriver <br> SurfaceThermalPolicy <br> Surfacetimealarmacpifilter <br> SurfaceUcmUcsiHidClient | n/a       |
| **Surface Laptop 3 with Intel processor** | SurfaceUpdate\SerialIOGPIO <br> SurfaceUpdate\SerialIOI2C <br> SurfaceUpdate\SerialIOSPI <br> SurfaceUpdate\SerialIOUART <br> SurfaceUpdate\SurfaceHidMini <br> SurfaceUpdate\SurfaceSerialHub <br> SurfaceUpdate\SurfaceHotPlug <br> SurfaceUpdate\Itouch   | Importing the following folders enables full keyboard, trackpad, and touch functionality in PE: <br>  <br> SerialIOGPIO <br> SerialIOI2C <br> SerialIOSPI <br> SerialIOUART <br> itouch <br> Chipset <br> ChipsetLPSS <br> ChipsetNorthpeak <br> ManagementEngine <br> SurfaceAcpiNotify <br> SurfaceBattery <br> SurfaceDockIntegration <br> SurfaceHidMini <br> SurfaceHotPlug <br> SurfaceIntegration <br> SurfaceSerialHub <br> SurfaceService <br> SurfaceStorageFwUpdat |
| **Surface Laptop 2**| SurfacePlatformInstaller\Drivers\System\GPIO <br> SurfacePlatformInstaller\Drivers\System\SurfaceHIDMiniDriver <br> SurfacePlatformInstaller\Drivers\System\SurfaceSerialHubDriver <br> SurfacePlatformInstaller\Drivers\System\I2C <br> SurfacePlatformInstaller\Drivers\System\SPI <br> SurfacePlatformInstaller\Drivers\System\UART <br> SurfacePlatformInstaller\Drivers\System\PreciseTouch  | For newer .msi files beginning with "SurfaceUpdate", use: <br>  <br> SurfaceUpdate\SerialIOGPIO <br> SurfaceUpdate\serialioi2c <br> SurfaceUpdate\SerialIOSPI <br> SurfaceUpdate\SerialIOUART <br> SurfaceUpdate\SurfaceHidMini <br> SurfaceUpdate\SurfaceSerialHub <br> SurfaceUpdate\Itouch      |
| **Surface Laptop (1st Gen)**  | SurfacePlatformInstaller\Drivers\System\GPIO <br> SurfacePlatformInstaller\Drivers\System\SurfaceHidMiniDriver <br> SurfacePlatformInstaller\Drivers\System\SurfaceSerialHubDriver <br> SurfacePlatformInstaller\Drivers\System\PreciseTouch   | For newer .msi files beginning with **"SurfaceUpdate"**, use: <br>  <br> SurfaceUpdate\SerialIOGPIO <br> SurfaceUpdate\SurfaceHidMiniDriver <br> SurfaceUpdate\SurfaceSerialHubDriver <br> SurfaceUpdate\Itouch    |

### Surface Pro 11 - Intel

In addition to the folders listed here, you also need to include the folder `SurfaceHidMini_WinPE_Intel` from this downloadable zip file. The included `Readme.txt` contains additional information.

<details>
<summary>Folders</summary>

```
acpiplatformextension
apoextension
aposwcinstaller
batteryclient
batteryminiport
bluetooth
Button
chipset
displayhardware
dspextension
HotPlug
ialpss2gpio2
ialpss2i2c
ialpss2i3clnl
ialpss2spilnl
ialpss2uart2lnl
intcpmt
Integration
msu53cx22x64sta
msu56cx22x64sta
oobpairingoptinpackage
panel
SarManager
SerialHub
Service
SMFClient
smfdisplayclient
timealarmacpifilter
wifi
```
</details>

---

### Surface Pro 10 5G

In addition to the folders listed here, you also need to include the folder `SurfaceHidMini_WinPE_Intel` from this downloadable zip file. The included `Readme.txt` contains additional information.

<details>
<summary>Folders</summary>

```
5gnrcoexmgr
5gnrcoexmgrext
AcpiPlatformExtension
Battery
BtFilter
Button
gnss
GtoPatchDrvUMDFext
HotPlug
ialpss2_gpio2_mtl
ialpss2_i2c_mtl
ialpss2_spi_mtl
ialpss2_uart2_mtl
IhvCpuSmfClient
iigdextgoa
Integration
IntelQuickSPI
mbbnetadapter
mhihost
miscBtExtx64
miscWlanExtx64
msu53cx22x64sta
msu56cx22x64sta
PenWirelessChargerHotkey
PowerTrackerCore
psautoreg
qcwlan64
QmuxMdm
RadioTelemetry
Sarmanager
SerialHub
Service
SmfClient
SmfDisplayClient
SystemManagementFramework
systemtelemetrydriverusermode
thermalmdm
TimeAlarmAcpiFilter
TouchPenProcessor0C9DUpdate
TypeCoverV7FprUde
UcmUcsiHidClient
ude
```
</details>

---

### Surface Laptop 7 - Intel

In addition to the folders listed here, you also need to include the folder `SurfaceHidMini_WinPE_Intel` from this downloadable zip file. The included `Readme.txt` contains additional information.

<details>
<summary>Folders</summary>

```
acpiplatformextension
batteryclient
batteryminiport
bluetooth
Button
chipset
displayhardware
HotPlug
ialpss2gpio2
ialpss2i2c
ialpss2i3clnl
ialpss2spilnl
ialpss2uart2lnl
intcpmt
integration
msu53cx22x64sta
msu56cx22x64sta
oempanelcustomization
panel
quickspi
SarManager
SerialHub
Service
SMFClient
smfdisplayclient
surfacetouchpadprocessorupdate
timealarmacpifilter
touchpadg7cfuoverhidextnpackage0c9f
wifi
```
</details>

---

### Surface Pro 11 and Surface Pro 11 5G - ARM

In addition to the folders listed here, you also need to include the folder `SurfaceHidMini_WinPE_ARM` from this downloadable zip file. The included `Readme.txt` contains additional information.

<details>
<summary>Folders</summary>

```
5gnrcoexmgr
5gnrcoexmgrext
acpiplatformextension
acsp
apoextension
aposwcinstaller
appcompanionextensionpackage
asdext
aucdext
audiominiext
battery
button
camauxsensor
camauxsensorextension
camavs
camavsproext
camfrontsensor
camfrontsensorextension
camplatformext
camrearsensor
camrearsensorextension
cfuoverhid
dax3extqc
dax3swchsaarm64
devicestelemetryservicedriver
digitizerwotextnpackage
displayhardware
dppsext
dxext
gnss
gtopatchdrvumdfext
hidfriendlynames
hotplug
ihvaudiofilter
ihvcpusmfclient
integration
machinelearningservicenull
mbbfwupdate
mbbnetadapter
mhihost
miscbtext
miscwlanext
msu53cx22arm64sta
msu56cx22arm64sta
nfcclient
null
nxpnfcclientdriverext
oempanelcustomizationlcd
oempanelcustomizationoled
panel
pen0c0ffirmwareupdate
penblelcaddradaptation
penwirelesschargerhotkey
powermeter
powerstate
powertrackercore
proextadsp
prosnscfgcrd
psautoreg
qcabd
qcadc
qcadcm
qcadsprpc
qcadsprpcd
qcasd
qcasdapo
qcaucd
qcaudminiportapo
qcaudminiportbase
qcbluetooth
qcbtacxtransportdriver
qcbtaddvscregistry
qccamflash
qccamflashext
qccamisp
qccamispext
qccamjpege
qccammipicsi
qccammipicsiext
qccamplatform
qccamsecureisp
qccamsecureispext
qccdi
qcconnectionsecurity
qcdcf
qcdpps8380
qcdx
qceva
qcevaext
qcfgbcl
qcfgbclext
qcglink
qcgpi
qcgpio
qci2c
qciommu
qciommuext
qcipcc
qcipcrouter
qckmbam
qcnspmcdm
qcpdsr
qcpepwd
qcpil
qcpilext
qcpilfilterext
qcpmic
qcpmicapps
qcpmicext
qcpmicglink
qcpmicgpio
qcppx
qcrpen
qcscm
qcsecapp
qcsensors
qcskext
qcslimbus
qcsmmu
qcsocpartition
qcsp
qcspi
qcspmi
qcssgservicesumd
qcsubsys
qcsubsysextcdsp
qcsubsysextspss
qcsubsysthermalmgr
qcsyscache8380
qctftpkmdf
qctree
qctreeextqcom
qcuart
qcursext
qcusb4bus
qcusb4filter
qcusbcucsi
qcusbfnssfilter
qcwlanhmt
qcwlanhmtext
qcwwanpowerdown
qcxhcifilter
qmuxmdm
radiotelemetry
sar
serialhub
service
smfclient
smfdisplayclient
spiextden
storagefwupdateenum
storagefwupdatehfs001tej3x108n
storagefwupdatehfs256gej3x108n
storagefwupdatehfs512gej3x108n
storagefwupdatekbg50zns1t
storagefwupdatekbg50zns256g
storagefwupdatekbg50zns512g
storagefwupdatemz9l41t0hblb00bmv
storagefwupdatemz9l4256hcjq00bmv
storagefwupdatemz9l4512hblu00bmv
storagefwupdatesddptqd1t001124
storagefwupdatesddptqd256g1124
storagefwupdatesddptqd512g1124
systemmanagementframework
systemtelemetryusermode
thermalmdm
thermalpolicy
thunderbolt4dockfwupdate
timealarmacpifilter
touchg6fwupdateextnpackage0c80
touchg6fwupdateextnpackage0c83
touchpadg7cfuoverhidextnpackage
touchpadsettingsextensionpackage
touchpenprocessor0c80update
touchpenprocessor0c83update
typecoverv7fprude
typecoverv7fwupdate
ucmucsihidclient
ude
wbfusbdriver
```
</details>

---

### Surface Laptop 7 - ARM

In addition to the folders listed here, you also need to include the folder `SurfaceHidMini_WinPE_ARM` from this downloadable zip file. The included `Readme.txt` contains additional information.

<details>
<summary>Folders</summary>

```
acpiplatformextension
battery
button
ccdi8380
dax3extqc
dax3swchsaarm64
DevicesTelemetryServiceDriver
digitizerwotextnpackage
hotplug
ihvcpusmfclient
miscbtext
miscwlanext
msu53cx22arm64sta
msu56cx22arm64sta
null
nullcapsule
powertrackercore
proextadsp8380
qcabd
qcadc8380
qcadsprpc8380
qcbluetooth8380
qcbtacxtransportdriver8380
qcbtaddvscregistry8380
qcconnectionsecurity
qcdcf
qcfgbcl8380
qcfgbclext8380
qcglink8380
qcgpi8380
qcgpio8380
qci2c8380
qciommu
qciommuext8380
qcipcc8380
qcipcrouter8380
qckmbam8380
qcnspmcdm8380
qcpdsr
qcpepwd8380
qcpil
qcpilext8380
qcpilfilterext
qcpmic8380
qcpmicapps8380
qcpmicext8380
qcpmicglink8380
qcpmicgpio8380
qcppx8380
qcrpen
qcscm
qcsecapp
qcskext8380
qcslimbus8380
qcsmmu8380
qcsocpartition
qcsp8380
qcspi8380
qcspmi8380
qcssgservicesumd
qcsubsys8380
qcsubsysextcdsp8380
qcsubsysextspss8380
qcsubsysthermalmgr
qcsyscache8380
qctftpkmdf
qctree
qctreeextqcom8380
qcuart8380
qcursext
qcusb4bus8380
qcusb4filter8380
qcusbcucsi8380
qcusbfnssfilter8380
qcwlanhmt8380
qcwlanhmtext8380
qcxhcifilter8380
rtsper
sar
service
smfclient
storagefwupdateenum
storagefwupdatehfs001tej3x108n
storagefwupdatehfs256gej3x108n
storagefwupdatehfs512gej3x108n
storagefwupdatekbg50zns1t
storagefwupdatekbg50zns256g
storagefwupdatekbg50zns512g
storagefwupdatemz9l41t0hblb00bmv
storagefwupdatemz9l4256hcjq00bmv
storagefwupdatemz9l4512hblu00bmv
storagefwupdatesddptqd1t001124
storagefwupdatesddptqd256g1124
storagefwupdatesddptqd512g1124
surfacehidfriendlynames
surfaceintegrationdriver
surfacepowermeter
surfacepowerstate
surfaceserialhubdriver
surfacetouchpadg7cfuoverhidextnpackage
surfacetouchpadprocessorupdate
systemmanagementframework
systemtelemetryusermode
thermalpolicy
Thunderbolt4DockFWUpdate
ucmucsihidclient
```
</details>

### Surface Laptop 6

<details>
<summary>Import folders</summary>

```
ialpss2gpio2mtl
ialpss2i2cmtl
ialpss2spimtl
ialpss2uart2mtl
intcpmt
intelquickspi
msu53cx22x64sta
msu56cx22x64sta
surfaceacpiplatformextension
surfacebattery
surfacebutton
surfacedockintegration
surfacehidminidriverwinre
surfacehotplug
surfaceintegrationdriver
surfacepanel
surfacepen217integration
surfacepenblelcaddradaptationdriver
surfaceserialhub
surfaceservicenulldriver
surfacesptclient
surfacetimealarmacpifilter
surfacetouchpenprocessor0c88update
surfacetouchpenprocessor0c89update
surfaceucmucsihidclient
tbtslimhostcontroller
```
</details>

**More information**: If you're using a Windows 10 version of Windows PE and you need Surface Ethernet connectivity, you also need to import the folder “msump64x64sta” from the Windows 10 MSI.

---

### Surface Pro 10

<details>
<summary>Import folders</summary>

```
acpiplatformextension
Battery
DockIntegration
HidMini
HotPlug
ialpss2gpio2mtl
ialpss2i2cmtl
ialpss2spimtl
ialpss2uart2mtl
Integration
IntelQuickSPI
msu53cx22x64sta
msu56cx22x64sta
penwirelesschargerhotkey
SarManager
SerialHub
Service
SMFClient
smfdisplayclient
timealarmacpifilter
UcmUcsiHidClient
```
</details>

**More information**: If you're using a Windows 10 version of Windows PE and you need Surface Ethernet connectivity, you also need to import the folder “msump64x64sta” from the Windows 10 MSI.

---

### Surface Pro 9 with Intel processor

<details>
<summary>Import folders</summary>

```
adlserial
alderlakepchpsystem
alderlakesystem
gna
intelprecisetouch
managementengine
msump64x64sta
surfaceacpiplatformextension
surfacebattery
surfacedockintegration
surfacehidmini
surfacehotplug
surfaceintegrationdriver
surfacesarmanager
surfaceserialhubdriver
surfaceservicenulldriver
surfacetimealarmacpifilter
surfaceucmucsihidclient
tbtslimhostcontroller
```
</details>

---

### Surface Laptop Studio 2

<details>
<summary>Import folders</summary>

```
Adl-rplserialLPSS
cardreader
heci
intelquickspi
msu53cx22x64sta
realtekEthernet
surfaceacpiplatformextension
surfacebattery
surfacedockintegration
surfacehidminidriver
surfacehotplug
surfaceintegrationdriver
surfacepenwirelesschargerhotkey
surfacesarmanager
surfaceserialhub
surfacesptclient
surfacetimealarmacpifilter
surfaceucmucsihidclient
surfacewakeontouchcontrol
wotquickspiextensionport1
```
</details>
