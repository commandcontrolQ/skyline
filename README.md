# Windows codename Neptune
Windows codename Neptune is a modified version of Windows 10 Pro (22H2)

# Features


# Disclaimers
- This software is not affiliated with Microsoft.
- This software will not be preactivated. You will need a valid license key.
- The Microsoft Store, as well as most builtin UWP apps, are removed.
  > To reinstall the Microsoft Store, run the following command in an elevated PowerShell process:
  > 
  > `Get-AppXPackage *WindowsStore* -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register “$($_.InstallLocation)\AppXManifest.xml”}`
- Sometimes, when Windows updates, it can revert any tweaks or reinstall bloatware such as Microsoft Edge and its WebView2 runtime. To prevent this from happening, **automatic updates are disabled by default.** This means that you will not be able to access the latest security hotfixes.
  - **With respect to people's security, the ability to update has not been removed entirely, but merely disabled.** If you want to enable automatic updates anyways, you can do this by enabling the Windows Update service (otherwise known as 'wuauserv'). This can be done using the Services MMC Snap-In, or by running the following command in an elevated terminal: `sc config wuauserv start=auto && sc start wuauserv`
