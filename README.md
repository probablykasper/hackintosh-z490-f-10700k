### Todos / Personal notes
- Windows installation will mess up the OpenCore EFI partition. To prevent, unplug all drives. M.2 drives can be disabled by using an invalid configuration in UEFI `Advanced`/`Onboard Devices Configuration` (for example configure an NVMe drive as SATA). If the EFI does get messed up, simply boot using a USB drive, mount the EFI and paste in the correct EFI.
- Perhaps change to 4096 allocation block size. Check default KC3000 allocation block size.
- Fix hardware acceleration. https://dortania.github.io/OpenCore-Post-Install/universal/drm.html#testing-hardware-acceleration-and-decoding
- Fix fans sleep. Maybe `sudo pmset -a hibernatemode 25`.

### Sonoma installation boot loop fix
`SecureBootModel` needs to be set to `Disabled` during the install process, and can be set back to `Default` after. Explanations:
- https://github.com/dortania/OpenCore-Install-Guide/pull/463/files
- https://github.com/dortania/OpenCore-Install-Guide/pull/473/files

### Sleep settings
- `sudo pmset proximitywake 0`
- `sudo pmset hibernatemode 0`

### Mount EFI
`./Hackintosh/MountEFI/MountEFI.command MacHD`

### BIOS
- Enabled Intel (VMX) Virtualization Technology
- Enabled VT-d
- Enabled PTT
- Disabled Serial Port
- Disabled Fast Boot
- Resizable bar off

## Hardware
- 10700k
- Intel UHD Graphics 630 (30.0.100.9805)
- Dedicated GPU: PowerColor Red Devil RX 6600 XT 8GB GPU
- Chipset: Z490
- ASUS ROG Strix Z490-F
- Intel Ethernet Controller I225-V #2

## Audio
Realtek ALC S1220A (PCI ID 10EC,1168)

Layout IDs:
- 1,2 Too loud
- 3,5 idk
- 7 Good
- 8,11,13,15,20,21,99 idk

## Storage
- Samsung 980 1TB (M.2_2 NVMe SSD)
- Kingston SKC2000M8250G 250GB (M.2_1 NVMe SSD)
- Kingston SV300S37A240G 240GB (SATA AHCI SSD)
- ST1000DM010-2EP102 1TB (SATA AHCI HDD)
- Samsung 850 EVO 120GB (SATA AHCI SSD)

## USB
Back:
- Port 13: USB2 (BIOS)
- Port 12: USB2
- Port 1/2/3+17+18+19: USB3 (3.2gen2 red)
- Port 4+20: USB-C 3 with switch (3.2gen2)
- Port 9/10+25/26: USB3 (3.2gen1 blue)
Front:
- Port 5+21: USB-C 3 with switch
- Port 6: USB2 (x2) hub
- Port 7/8+23/24: USB3
3000USB (internal)
- Port 11: USB2 (Used by AURA LED controller)

## Bios
- Enabled Intel (VMX) Virtualization Technology
- Enabled VT-d
- Enabled PTT
- Disabled Serial Port
- Disabled Fast Boot
- Resizable bar off
