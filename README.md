# Asrock-Z690-PG-Reptide-hackintosh
EFI OpenCore and Clover Folders

Attention! If you have RX5700 (XT) graphics card, you have to use the nameframe (ATI,Adder) to avoid WindowServer crashes!

## Hardware configuration:
* CPU: i7-12700kf AlderLake
* MB: Asrock Z690 PG Reptide [More info](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#Overview). 
* RAM: 2x32Gb DDR4 3200 Crucial Technology      
* GPU: Radeon Sapphire Nitro+ RX5700XT 8G GDDR6 SE [More info](https://www.sapphiretech.com/ru-ru/consumer/nitro-radeon-rx-5700-xt-se-8g-gddr6).
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - macOS Tahoe 26.2 (2C56).
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - Windows 11 (25H2).
* SSD: Samsung 860 EVO 500GB (SATA-6 AHCI) - macOS Ventura 13.7.8 (22H730).
* WIFI / BT: BCM94360 FENVI FV-HB1200 AC PCI-E adapter.
* For full functionality FENVI FV-HB1200 on Mac OS Sonoma and Sequoya, required:
* [OCLP patch 2.4.1 or newer](https://github.com/dortania/OpenCore-Legacy-Patcher).
* For full functionality FENVI FV-HB1200 on macOS Tahoe, required:

## [OpenCore Legacy Patcher 3.0.0 Experimental](https://github.com/YBronst/OpenCore-Legacy-Patcher/releases/tag/3.0.0).
* Discussion of this patch [English forum](https://www.insanelymac.com/forum/topic/362042-experimental-fork-of-oclp-300-nightly-–-wi-fi-airdrop-and-applehda-fully-working-under-tahoe/)

## Application issues
* System version mismatch error when root patching
* Use an experimental ["PurgePendingUpdate" tool](https://github.com/YBronst/Asrock-Z690-PG-Reptide/blob/main/purgePendingUpdate.zip) 

## Uninstall

This guide tells you different ways to uninstall OCLP and/or patches.

### Manual methods

Uninstalling OCLP manually is a three part process which includes the application, and the root patches. If you want to remove OCLP and patches entirely, go through all three in succession. Otherwise do the part(s) you need.

### Reverting root patches

Open the OCLP application and go into the Post Install Root Patch menu, choose Revert Root Patches. 

*  **Supported on Monterey and later. Big Sur does not support snapshot reversion and requires a reinstall.**
*  **Reinstall can be done without a wipe if the macOS installer version used is the same or newer.**

### Uninstalling the application

To uninstall the OCLP application including LaunchAgent and PrivilegedHelperTool, download the uninstaller package from [the releases page.](https://github.com/dortania/OpenCore-Legacy-Patcher/releases)

### Update BIOS: [21.01	2025/10/30	10.80MB](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#BIOS)

* 1. Optimized system compatibility.
* 2. Enhance platform security with Control IOMMU Pre-boot Behavior, VT-d, and the IOMMU option.

### BIOS setup: 

* Default

### All archives of bootable EFI folders have already been updated to the latest versions of OpenCore and Clover but you can download them:
* [OpenCore loader 1.0.7](https://github.com/dortania/build-repo/releases/download/OpenCorePkg-507907a/OpenCore-1.0.7-RELEASE.zip) 
* [Clover 5165](https://github.com/YBronst/CloverBootloader/releases/tag/5165)


## ❗️Warning
* FileVault2 not working in Sonoma/Sequoia and Tahoe with the OCLP patch!
 
## 📝 Notes
* All mac os futures are working including DRM playback and sleep/wake S3 and FileVault2 in macOS Ventura 13.x.x versions.
* Clover has issue with update under T2 mac models
* Before use, you need to generate your own MLB and SMBIOS data using a Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist [More info](https://github.com/corpnewt/GenSMBIOS)
