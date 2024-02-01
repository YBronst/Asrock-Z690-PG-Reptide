# Asrock-Z690-PG-Reptide-hackintosh
EFI OpenCore and Clover Folders

Attention! If you have RX5700 (XT) graphics card, you have to use the nameframe (ATI,Adder) to avoid WindowServer crashes!

## Hardware configuration:
* CPU: i7-12700kf AlderLake
* MB: Asrock Z690 PG Reptide [More info](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#Overview) 
* RAM: 2x32Gb DDR4 3200 Crucial Technology      
* GPU: Radeon Sapphire Nitro+ RX5700XT 8G GDDR6 SE [More info](https://www.sapphiretech.com/ru-ru/consumer/nitro-radeon-rx-5700-xt-se-8g-gddr6)
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - macOS Sonoma 14.3
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - Windows 11
* SSD: Samsung 860 EVO 500GB (SATA-6 AHCI) - macOS Ventura 13.6.4
* WIFI / BT: FENVI FV-HB1200 AC PCI-E BCM94360CS2 Bluetooth-compatible4.0, 802.11AC adapter [More info](https://fenvi.com/product_detail_32.html) 
* BIOS: [v17.03 2024/1/15 10.78MB](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#BIOS)
* 1. Patch UEFI LogoFail vulnerabilities.
* 2. Optimize processor settings.
* 3. Optimize BIOS settings.
* Display: ViewSonic VX3211-4K-mhd 60 Hz HDR via Display Port

### BIOS setup: 

* Default

### Mac OS Monterey and Ventura EFI OpenCore loader 0.9.8 and Clover 5157
### Mac OS Sonoma with EFI OpenCore loader 0.9.8 and Clover 5157 + legacy Broadcom WiFi + OCLP patch 1.3.0

FileVault2 not working in Sonoma with the OCLP patch!
 
* All mac os futures are working including DRM playback and sleep/wake S3 and FileVault2
* Clover has issue with update under T2 mac models

* Before use, you need to generate your own MLB and SMBIOS data using a Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist [More info](https://github.com/corpnewt/GenSMBIOS)
