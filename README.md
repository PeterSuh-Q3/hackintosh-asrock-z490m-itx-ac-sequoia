Equipment:
- AsRock z490m itx/ac motherboard
- Intel i7-10700 processor
- AMD Radeon RX 6600 XT 8 GB graphics card
- Monitor with a resolution of 2560x1440
- BCM4360 WIFI/BT

BY:
- OpenCore 0.9.7
- Sonoma 14.4.1

Works:
- Dual ethnernet (1.0Gbps, 2.5Gbps)
- WiFi (After removing the motherboard built-in Intel M.2 WiFi model, replace BCM4360, apply sonoma IO kext patch for OCLP)
- Bluetooth (BCM4360)
- USB ports (rear and front)
- Sleep
- iCloud, AppStore
- iMessage, Facetime
- Sound via 3.5 and HDMI
- DRM

Version 1.1
- Fix iServices

Version 1.2
- Updated OpenCore to version 0.6.7
- Updated Lilu, WhateverGreen, VirtualSMC, SMCSuperIO and SMCProcessor to versions current as of March 31, 2021
- Added a graphical interface to the bootloader, hidden unnecessary menu items (recovery, reset nvram, etc)

Version 1.3
- Updated AirportItlwm to version 1.3. Wi-Fi speed is no longer limited to 40 Mbit/s.

Version 1.4
- Removed Usbinjectall
- Added by Usbmap
- Set xhciportlimit = false for compatibility with Big Sur 11.3 and higher

Version 1.5
- Updated OpenCore to version 0.7.2
- Updated AirportItlwm, AppleALC, Lilu, NVMeFix, SMCProcessor, SMCSuperIO, VirtualSMC, WhateverGreen to the latest versions as of August 13, 2021

Version 1.6
- Removed FakePCIID and FakePCIID_Intel_HDMI_Audio.kext due to conflicts with Monterey
- Updated AirportItlwm, AppleALC, Lilu, WhateverGreen, VirtualSMC, SMCSuperIO and SMCProcessor to the latest versions as of May 7, 2022
- Added IntelBluetoothFirmware to fix Bluetooth (unsuccessful)
- The config was rewritten from scratch to avoid problems with updating to Monterey

Version 1.6.1
- Added BlueToolFixup, now Bluetooth works

Version 1.6.2
- Added FakePCIID and FakePCIID_Intel_HDMI_Audio to restore sound from the repository
https://github.com/mbarbierato/OS-X-Fake-PCI-ID/releases/tag/v1.3.16

Version 1.7
- Updated OpenCore to version 0.8.8
- Added support for external video card RX 6600XT
- Updated AppleALC, Lilu, NVMeFix, WhateverGreen, VirtualSMC, SMCSuperIO and SMCProcessor to the latest versions as of January 3, 2023

Version 1.7.1
- Removed FakePCIID and FakePCIID_Intel_HDMI_Audio.kext, audio now works natively
- Removed NullEthernet
- Fixed problems with DRM, to activate you need to run the command in the terminal

``defaults write com.apple.AppleGVA gvaForceAMDKE -boolean yes``

Version 1.8
- Updated OpenCore to version 0.9.5
- Updated AirportItlwm, AppleALC, BlueToolFixup, IntelBluetoothFirmware, Lilu, RadeonSensor, SMCRadeonGPU, WhateverGreen, VirtualSMC, SMCSuperIO and SMCProcessor to the latest versions as of September 16, 2023

Version 1.9
- Updated OpenCore to version 0.9.7
- Updated AppleALC to the latest version as of January 4, 2024

Version 2.0
- Added IntelMausi.kext and LucyRTL8125Ethernet.kext for dual internal ethnernet (1.0Gbps, 2.5Gbps)
- Apply Sonoma IO kext patch for BCM4360 (requires OCLP 1.4.3)

Version 2.1
- Added AMFIPass.kext (Use Instead of AMFI=0x80) and removed NVMeFix.kext to solve AMFI issues in Sonoma
- Removed AMFI=0x80 to solve AMFI issues in Sonoma

Issues in Version 2.0:
- VMWare (unable to boot; check normal operation after applying AMFIPass)
- Firefox (does not run; check if it can run after applying AMFIPass)
- Creative Cloud Apps (CC5.9, Illustrator28.2 crashes when opening file; confirmed normal operation after applying AMFIPass)
- League of Legends (Available after applying AMFIPass)
- RIDIBooks (not running; confirm normal operation after applying AMFIPass)
- Skype (not running; confirm normal operation after applying AMFIPass)
- Electron-based Apps
- Other apps that should not disable AMFI after disabling SIP.

SMBIOS removed, need to generate serial numbers

The configuration is posted for informational/educational purposes. I do not guarantee performance on equipment other than mine.
