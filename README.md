# unattend.xml
unattend.xml for use with Ventoy

# Download the file
```batch
mkdir %userprofile%/Downloads/Templates
cd %userprofile%/Downloads/Templates
PowerShell -ExecutionPolicy Unrestricted -Command "irm -Uri https://github.com/thomaslinux/unattend.xml/raw/refs/heads/main/unattend.xml -outfile unattend.xml"
```

# Reset with unattend from running PC
1. Disable bitlocker
2. Uninstall Sentinel One (if impossible, goto Reset from oobe)
1. Open Templates folder on your usb key and run ``ADMIN reset.cmd``
2. Reset should happen with unattend

# Reset from oobe
After asking the PC for reset, on OOBE screen
Shift + F10
Focus the cmd window (Alt + Tab) or click on it
```batch
D:
cd Templates
"ADMIN reset.cmd"
```

# Credits
Me
https://schneegans.de/windows/unattend-generator/
