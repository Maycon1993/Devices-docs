---
title: Use the Surface Hub Hardware Diagnostic Tool to test a device account
description: Use the Surface Hub Hardware Diagnostic Tool to test a device account, verify connectivity, and troubleshoot environment and certificate issues.
ms.assetid: a87b7d41-d0a7-4acc-bfa6-b9070f99bc9c
ms.service: surface-hub
author: coveminer
ms.author: chauncel
ms.topic: how-to
ms.localizationpriority: medium
ms.date: 06/09/2020
---

# Use the Surface Hub Hardware Diagnostic Tool to test a device account

## Introduction

> [!NOTE]
> The Account Settings section of the Surface Hub Hardware Diagnostic tool doesn't collect any information. Email and password inputs are used only within your environment and are never collected or transmitted. Sign-in details persist only for the current session and are cleared when the app is closed or the session ends.

> [!IMPORTANT]
>
> * Administrator privileges aren't required to run this application.
> * The results of the diagnostic should be discussed with your local administrator before you open a service call with Microsoft.

### Surface Hub Hardware Diagnostic

By default, the [Surface Hub Hardware Diagnostic](https://www.microsoft.com/store/apps/9nblggh51f2g) application isn’t installed in earlier versions of the Surface Hub system. The application is available for free from the Microsoft Store. Administrator privileges are required to install the application.

   ![Screenshot of Hardware Diagnostic.](images/01-diagnostic.png)

## About the Surface Hub Hardware Diagnostic Tool

The Surface Hub Hardware Diagnostic tool is an easy-to-navigate tool that lets the user test many of the hardware components within the Surface Hub device. This tool can also test and verify a Surface Hub device account. This article describes how to use the Account Settings test within the Surface Hub Hardware Diagnostic tool.

> [!NOTE]
> The device account for the Surface Hub should be created before any testing is done. The Surface Hub Administrator Guide provides instructions and PowerShell scripts to help you create on-premises, online (Office365), or hybrid device accounts. For more information, go to the [Create and test a device account (Surface Hub)](/surface-hub/create-and-test-a-device-account-surface-hub) article in the guide.

### Device account testing process

1. Navigate to **All Apps**, and then locate the Surface Hub Hardware Diagnostic application.

    ![Screenshot of  All Apps.](images/02-all-apps.png)

1. When the application starts, the **Welcome** page provides a text window to document the reason why you're testing the Hub. This note can be saved to USB together with the diagnostic results at the conclusion of testing. After you finish entering a note, select **Continue**.

    >[!NOTE]
    >When saving diagnostic results, don't change the default path or select a subdirectory. The files can be copied later via the File Explorer app.

    ![Screenshot of  Welcome.](images/03-welcome.png)

1. The next screen provides you with the option to test all or some of the Surface Hub components. To begin testing the device account, select the **Test Results** icon.

    ![Screenshot of  Test Options.](images/04-test-results-1.png)

    ![Screenshot of  Test Results.](images/05-test-results-2.png)

1. Select **Account Settings**.  

    ![Screenshot of  Account Settings.](images/06-account-settings.png)

    The Account Settings screen is used to test your device account.

    ![Screenshot of  Account Settings Details.](images/07-account-settings-details.png)

1. Enter the email address of your device account. The password is optional but is recommended. Select the **Test Account** button when you're ready to continue.

    ![Screenshot of  Test Account.](images/08-test-account.png)

1. After testing is finished, review the results for the four areas of testing. Each section can be expanded or collapsed by selecting the Plus or Minus sign next to each article.

    **Network**

    ![Screenshot of Network.](images/09-network.png)

    **Environment**

    ![Screenshot of Environment.](images/10-environment.png)

    **Certificates**

    ![Screenshot of Certificates.](images/11-certificates.png)

    **Trust Model**

    ![Screenshot of Trust Model.](images/12-trust-model.png)

## Appendix

### Field messages and resolution

#### Network

| Field |Success |Failure |Comment |Reference |
|------|------|------|------|------|
| Internet Connectivity | Device has Internet connectivity |Device doesn't have Internet connectivity |Verifies Internet connectivity, including proxy connection | |
| HTTP Version |1.1 |1.0 |If HTTP 1.0 is found, it may cause issues with Windows Update and the Microsoft Store | |
| Direct Internet Connectivity |Device has a Proxy configured (for success)<br>Device has no Proxy configured (for failure) |N/A |Indicates whether the device is behind a proxy | |
| Proxy Address | | |If configured, returns proxy address | |
| Proxy Authentication | Proxy doesn't require Authentication | Proxy requires Proxy Auth |May return a false positive if the user is already authenticated in an open Microsoft Edge session. | |
| Proxy Auth Types | | |If proxy authentication is used, return the Authentication methods advertised by the proxy | |

#### Environment

| Field |Success |Failure |Comment |Reference |
|------|------|------|------|------|
| SIP Domain | | |Informational  | |
| Skype Environment |Skype for Business Online, Skype for Business on-premises, Skype for Business Hybrid |Informational |What type of environment was detected. Note: Hybrid can only be detected if the password is entered. | |
| LyncDiscover FQDN | | |Informational: Displays the LyncDiscover DNS result | |
| LyncDiscover URI | | |Informational: Displays the URL used to perform a LyncDiscover on your environment| |
| LyncDiscover |Connection Successful |Connection Failed |Response from LyncDiscover web service. | |
| SIP Pool Hostname | | |Informational: Display the SIP pool name discovered from LyncDiscover | |

#### Certificates (on-premises hybrid only)

LyncDiscover Certificate

| Field |Success |Failure |Comment |Reference |
|------|------|------|------|------|
| LyncDiscover Cert CN | | |Informational: Displays the LD certificate common name | |
| LyncDiscover Cert CA | | |Informational: Displays the LD Cert CA | |
| LyncDiscover Cert Root CA | | |Informational: Displays the LD Cert Root CA, if available | |
| LD Trust Status |Certificate is trusted |Certificate isn't trusted: Add the Root CA |Verify the certificate against the local certificate store. Returns positive if the machine trusts the certificate|[Download and deploy Skype for Business certificates using PowerShell](https://blogs.msdn.microsoft.com/surfacehub/2016/06/07/download-and-deploy-skype-for-business-certificates-using-powershell/)/[Supported items for Surface Hub provisioning packages](/surface-hub/provisioning-packages-for-surface-hub#supported-items-for-surface-hub-provisioning-packages) |

SIP Pool Certification

| Field | Success | Failure | Comment | Reference |
|------|------|------|------|------|
| SIP Pool Cert CN | | |--- | |
| SIP Pool Cert CA | | |--- | |
| SIP Pool Trust Status |Certificate is trusted |Certificate isn't trusted: Add the Root CA |Verify the certificate against the local cert store and return a positive if the devices trust the certificate | |
| SIP Pool Cert Root CA | | |Information: Displays the SIP pool certificate root CA, if available | |

#### Trust Model (on-premises hybrid only)

| Field | Success | Failure | Comment | Reference |
|------|------|------|------|------|
| Trust Model Status |No Trust Model Issue Detected |SIP domain and server domain are different: Add the following domains |Check the LD FQDN/ LD Server Name/ Pool Server name for Trust model issue.  | |
| Domain Names | | |Return the list of domains that should be added for SFB to connect | |
