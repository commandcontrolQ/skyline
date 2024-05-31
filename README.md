# Windows codename Skyline
Windows codename Skyline is a modified version of Windows 10 IoT Enterprise LTSC 2021.

# Features
- Brought back the original Windows 7 games (credits to Winaero Tweaker) and all 4 Windows Entertainment Packs (courtesy of [this archive.org link](https://archive.org/details/wep_20200803)). The 4 WEP games are located in `%USERPROFILE%\Saved Games`.
  - Bundled in `%SYSTEMDRIVE%\Windows` is WineVDM 0.9.0, which allows the execution of 16-bit programs. Credits to [otya128](https://github.com/otya128/).
- Bundles programs into the image using NTLite. These programs include:
  - 7-Zip
  - Transmission
  - LibreOffice
  - OpenVPN
  - PuTTY
  - HWiNFO
  - Resource Hacker
  - Process Hacker
  - IrfanView (32-bit)
  - HWiNFO
  - TreeSize Free
  - FileZilla
  - CrystalDisk Info
  - VLC media player
  - Pale Moon
  - QuiteRSS
  - QBittorrent
  - Free Download Manager
  - Winaero Tweaker
- Adds standalone programs into `%USERPROFILE%\Desktop\Other`. These include:
  - Rufus 4.1
  - Visual C++ all-in-one redistributable
  - 

# Disclaimers
- This software is not affiliated with Microsoft.
- This software will not be preactivated. You will need a valid license key.
- The Microsoft Store, as well as most builtin UWP apps, are removed.
  > To reinstall the Microsoft Store, run the following command in an elevated PowerShell process:
  > 
  > `Get-AppXPackage *WindowsStore* -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register “$($_.InstallLocation)\AppXManifest.xml”}`
- Sometimes, when Windows updates, it can revert any tweaks or reinstall bloatware such as Microsoft Edge and its WebView2 runtime. To prevent this from happening, **automatic updates are disabled by default.** This means that you will not be able to access the latest security hotfixes.
  - **With respect to people's security, the ability to update has not been removed entirely, but merely disabled.** If you want to enable automatic updates anyways, you can do this by enabling the Windows Update service (otherwise known as 'wuauserv'). This can be done using the Services MMC Snap-In, or by running the following command in an elevated terminal: `sc config wuauserv start=auto && sc start wuauserv`
