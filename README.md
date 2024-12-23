# Asrock-Z690-PG-Reptide-hackintosh
EFI OpenCore and Clover Folders

Attention! If you have RX5700 (XT) graphics card, you have to use the nameframe (ATI,Adder) to avoid WindowServer crashes!

## Hardware configuration:
* CPU: i7-12700kf AlderLake
* MB: Asrock Z690 PG Reptide [More info](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#Overview) 
* RAM: 2x32Gb DDR4 3200 Crucial Technology      
* GPU: Radeon Sapphire Nitro+ RX5700XT 8G GDDR6 SE [More info](https://www.sapphiretech.com/ru-ru/consumer/nitro-radeon-rx-5700-xt-se-8g-gddr6)
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - macOS Sequoia 15.2
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - Windows 11
* SSD: Samsung 860 EVO 500GB (SATA-6 AHCI) - macOS Ventura 13.7.2
* WIFI / BT: BCM94360 FENVI FV-HB1200 AC PCI-E adapter
* BIOS: [v20.02 2024/10/7 10.72MB](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#BIOS)
* Update CPU microcode to 0x12B.

### BIOS setup: 

* Default

### Mac OS Sequoia and Ventura EFI OpenCore loader 1.0.3 and Clover 5161
### Mac OS Sequoia with EFI OpenCore loader 1.0.3 and Clover 5161 + legacy Broadcom WiFi + OCLP patch 2.2.0

FileVault2 not working in Sonoma with the OCLP patch!
 
* All mac os futures are working including DRM playback and sleep/wake S3 and FileVault2
* Clover has issue with update under T2 mac models

* Before use, you need to generate your own MLB and SMBIOS data using a Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist [More info](https://github.com/corpnewt/GenSMBIOS)
