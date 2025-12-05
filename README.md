# Asrock-Z690-PG-Reptide-hackintosh
EFI OpenCore and Clover Folders

Attention! If you have RX5700 (XT) graphics card, you have to use the nameframe (ATI,Adder) to avoid WindowServer crashes!

## Hardware configuration:
* CPU: i7-12700kf AlderLake
* MB: Asrock Z690 PG Reptide [More info](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#Overview) 
* RAM: 2x32Gb DDR4 3200 Crucial Technology      
* GPU: Radeon Sapphire Nitro+ RX5700XT 8G GDDR6 SE [More info](https://www.sapphiretech.com/ru-ru/consumer/nitro-radeon-rx-5700-xt-se-8g-gddr6)
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - macOS Sequoia 15.7.2 (24G325)
* SSD: WD_BLACK SN850X 1000GB NVME M2 (PCI-e 4.0) - Windows 11
* SSD: Samsung 860 EVO 500GB (SATA-6 AHCI) - macOS Ventura 13.7.8 (22H730)
* WIFI / BT: BCM94360 FENVI FV-HB1200 AC PCI-E adapter
* For full functionality FENVI FV-HB1200 on Mac OS Sonoma and Sequoya, required OCLP patch 2.4.0 or newer
* BIOS: [v20.02 2024/10/7 10.72MB](https://pg.asrock.com/mb/Intel/Z690%20PG%20Riptide/index.ru.asp#BIOS)
* Update CPU microcode to 0x12B.

### BIOS setup: 

* Default

### Mac OS Sequoia and Ventura EFI OpenCore loader 1.0.6 and Clover 5163

The MacPro-OpenCore-1.0.7-Z690PG-R-12700kf-Tahoe.zip Partualy compatible with macOS 26 Tahoe (Wi-Fi doesn't work)
The MacPro-OpenCore-1.0.7-Z690PG-R-12700kf-Sequoia.zip fully compatible with macOS Ventura 13, macOS Sonoma 14 and macOS Sequoia 15.
The MacPro-Clover-5164-Z690PG-R-12700kf-Sequoia.zip is backward compatible with macOS Sonoma 14 (Just move the kexts from folder 15 to folder 14).
The MacPro-Clover-5164-Z690PG-R-12700kf-Ventura.zip for macOS Ventura 13 only. 

FileVault2 not working in Sonoma with the OCLP patch!
 
* All mac os futures are working including DRM playback and sleep/wake S3 and FileVault2 in macOS Ventura 13.x.x versions.
* Clover has issue with update under T2 mac models

* Before use, you need to generate your own MLB and SMBIOS data using a Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist [More info](https://github.com/corpnewt/GenSMBIOS)

* To try it, put the content folder 26 to the appropriate folder EFI on ESP
* Fenvi Wi-Fi: There is no solution yet, although OCLP developers are working on it.
* An Intel Wi-Fi can be used successfully instead (I've tested the AX210) but AirportItlwm.kext doesn't work in Tahoe and you must use itlwm.kext + Heliport app (latest versions of both).
