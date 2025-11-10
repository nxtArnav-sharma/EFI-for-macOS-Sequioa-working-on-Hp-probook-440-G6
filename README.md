# 💻 EFI for macOS Sequoia – HP ProBook 440 G6

This repository contains a fully functional EFI folder for **macOS Sequoia** running on the **HP ProBook 440 G6**.  
Tested and confirmed to boot, install, and run smoothly with working hardware components.

---

## 🧠 Overview

This EFI has been configured and tested specifically for:
- **Laptop:** HP ProBook 440 G6  
- **Processor:** Intel Core i5 / i7 (8th Gen – Whiskey Lake)  
- **GPU:** Intel UHD Graphics 620  
- **Bootloader:** OpenCore (latest version)  
- **macOS Version:** Sequoia (macOS 15)

---

## 💡 Hardware Compatibility

| Component | Model / Details | Status |
|------------|-----------------|--------|
| **CPU** | Intel Core i5-8265U / i7-8565U (Whiskey Lake) | ✅ Fully Working |
| **iGPU** | Intel UHD Graphics 620 | ✅ Full QE/CI Acceleration |
| **RAM** | Up to 32GB DDR4 | ✅ Fully Supported |
| **Storage** | SATA / NVMe SSD | ✅ Fully Working |
| **Wi-Fi / Bluetooth** | Intel Wireless-AC 9560 | ✅ Working (with AirportItlwm + IntelBluetoothFirmware) |
| **Audio Codec** | Realtek ALC236 | ✅ Working (AppleALC layout-id 11) |
| **Ethernet** | Realtek RTL8111 | ✅ Working (RealtekRTL8111.kext) |
| **Trackpad / Keyboard** | Synaptics PS2 | ✅ Working (VoodooPS2Controller.kext) |
| **Battery** | HP Integrated Battery | ✅ Working (SMCBatteryManager) |
| **Sleep / Wake** | System Sleep | ✅ Stable |
| **USB Ports** | All ports mapped | ✅ Working |
| **HDMI Output** | Video | ✅ Working |
| **HDMI Audio** | — | ✅ Working |
| **Fingerprint Reader** | Synaptics | 🚫 Not Working |
| **SD Card Reader** | Realtek | 🚫 Not Working |
| **Webcam** | Integrated 720p | ✅ Working |

---

## ⚙️ Working Features

✅ Intel UHD Graphics 620 acceleration  
✅ Wi-Fi and Bluetooth  
✅ Audio and microphone  
✅ Trackpad gestures and keyboard hotkeys  
✅ Sleep / Wake  
✅ Battery indicator  
✅ USB ports (properly mapped)  
✅ Brightness and volume control  
✅ iServices (App Store, iCloud, iMessage, FaceTime)

---

## ⚠️ Not Working / Untested

🚫 SD card reader  

---

## 📁 Folder Structure<br>

EFI/<br>
├── BOOT/<br>
└── OC/<br>
 &nbsp; ├── ACPI/<br>
 &nbsp; ├── Drivers/<br>
 &nbsp; ├── Kexts/<br>
 &nbsp; ├── Resources/<br>
 &nbsp; ├── Tools/<br>
 &nbsp; └── config.plist<br>

---

## 🧩 Recommended BIOS Settings

Before booting, enter BIOS and ensure:

| Setting | Value |
|----------|--------|
| Secure Boot | **Disabled** |
| Legacy Boot | **Disabled** |
| UEFI Boot Mode | **Enabled** |
| Fast Boot | **Disabled** |
| SATA Mode | **AHCI** |
| VT-d | **Disabled** *(or enable with `DisableIoMapper` quirk)* |
| Wake on LAN | **Disabled** |

---

## 🪄 Installation Tips

1. Prepare your macOS Sequoia USB installer using [macrecovery](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html) or [GibMacOS](https://github.com/corpnewt/gibMacOS).  
2. Mount the EFI partition of your USB.  
3. Copy this EFI folder to the USB’s EFI partition.  
4. Boot and install macOS Sequoia.  
5. After installation, mount your system drive’s EFI partition and copy this EFI there.  
6. Reboot — and enjoy a stable macOS experience on your HP ProBook 440 G6.

---

## 🧰 Credits

- [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)  
- [acidanthera](https://github.com/acidanthera) for OpenCore, Lilu, WhateverGreen, AppleALC, and VirtualSMC  
- [RehabMan](https://github.com/RehabMan) for early HP ProBook patches and ACPI guides  
- Hackintosh community contributors for continued testing and support

---

## 📢 Disclaimer

This EFI is **for educational and experimental purposes only.**  
Please ensure you have legitimate access to macOS.  
Use at your own risk — always back up your data before modifying your EFI or system.

---

### ✨ Author
**Arnav Sharma ([@nxtArnav-sharma](https://github.com/nxtArnav-sharma))**  
💬 Contributions, suggestions, and pull requests are welcome!
Please leave a star if you liked my work!


