# LtnOS 1.0 "Nebula"

A custom Linux distribution based on Arch Linux with GNOME Desktop.

## About

LtnOS is a polished operating system built on top of Arch Linux, combining the power and flexibility of Arch with a curated selection of software and configurations for an excellent out-of-the-box experience. LtnOS 1.0 "Nebula" features the complete GNOME Desktop Environment with over 150 pre-installed applications, custom theming, and Plymouth boot splash.

## Features

- **Arch Linux Foundation**: Built on the reliable and cutting-edge Arch Linux base
- **GNOME Desktop Environment**: Complete GNOME desktop with all extras and tweaks
- **Plymouth Boot Splash**: Beautiful animated boot screen
- **Custom GRUB Theme**: Branded bootloader with LtnOS logo
- **150+ Pre-installed Applications**: Everything you need out of the box
- **Rolling Release**: Enjoy continuous updates and the latest software packages
- **Full Hardware Support**: Intel/AMD microcode, extensive firmware, and all major graphics drivers (NVIDIA, AMD, Intel)
- **Developer-Ready**: Complete development tools for Python, Node.js, Rust, Go, Java, C/C++, and more
- **Multimedia Powerhouse**: Video editors (Kdenlive, Shotcut), audio production (Audacity, Ardour), and all codecs
- **Creative Suite**: GIMP, Inkscape, Krita, Blender, Darktable included
- **Gaming Support**: Wine, RetroArch, MAME, Dolphin, PPSSPP emulators pre-installed
- **Office Productivity**: LibreOffice, Thunderbird, multiple PDF viewers
- **Network Tools**: NetworkManager, VPN support, firewall utilities
- **Virtualization**: QEMU, libvirt, VirtualBox, Docker, Podman ready
- **Customizable**: Fully configurable to match your workflow and preferences

## System Requirements

- 64-bit processor (x86_64)
- Minimum 2 GB RAM (4 GB or more recommended)
- At least 20 GB of disk space (40 GB+ recommended for full functionality)
- UEFI or BIOS compatible system
- Internet connection for installation and updates
- USB drive with at least 8 GB for installation media

## Installation

### Prerequisites

- A bootable USB drive (minimum 8 GB)
- UEFI or BIOS compatible system

### Installation Steps

1. Download the latest LtnOS ISO from the releases page
   - Filename: `ltnos-1.0.0-nebula-x86_64.iso`
   - Verify the SHA256 checksum for integrity

2. Create a bootable USB drive:
   ```bash
   dd if=ltnos-1.0.0-nebula-x86_64.iso of=/dev/sdX bs=4M status=progress && sync
   ```
   Replace `/dev/sdX` with your USB device (use `lsblk` to identify)

   If you are in windows just use rufus and flash it :D

3. Boot from the USB drive
   - You'll see the custom GRUB theme with LtnOS branding

4. Follow the installation wizard

5. Enjoy the Plymouth boot splash on first boot

### Testing with QEMU

You can test the ISO in a virtual machine before installing:

```bash
qemu-system-x86_64 -enable-kvm -m 4G -cdrom ltnos-1.0.0-nebula-x86_64.iso -boot d
```

## Pre-installed Software

LtnOS comes with over 150 applications ready to use:

### Browsers
- Firefox
- Chromium
- GNOME Web (Epiphany)

### Office & Productivity
- LibreOffice Fresh (complete suite)
- Thunderbird (email)
- Evolution (email & calendar)
- Geary (lightweight email)

### Graphics & Design
- GIMP (photo editing)
- Inkscape (vector graphics)
- Krita (digital painting)
- Blender (3D modeling & animation)
- Darktable (RAW photo processor)
- Shotwell (photo manager)

### Multimedia
**Video Players**: VLC, MPV, Celluloid, SMPlayer  
**Music Players**: Rhythmbox, Lollypop, Audacious  
**Video Editors**: Kdenlive, Shotcut, Pitivi  
**Audio Editors**: Audacity, Ardour, LMMS  
**Screen Recording**: OBS Studio, Vokoscreen

### Development
**Editors**: VS Code, Vim, Neovim, Emacs, GNOME Builder  
**Languages**: Python, Node.js, Rust, Go, Java (8/11/17), C/C++, PHP, Ruby  
**Version Control**: Git, GitHub CLI, Mercurial, SVN  
**Containers**: Docker, Podman, Buildah  
**Virtualization**: QEMU, libvirt, VirtualBox  
**Databases**: MariaDB, PostgreSQL, Redis, SQLite

### Gaming & Emulation
- Wine (Windows compatibility)
- RetroArch (multi-system emulator)
- MAME, Dolphin, PPSSPP
- DOSBox, ScummVM
- GameMode (performance optimization)

### System Tools
- GParted (partition manager)
- Timeshift (system snapshots)
- GNOME Disks
- BleachBit (system cleaner)
- htop, btop (system monitors)
- File managers: Nautilus, Thunar, Dolphin

### Network & Communication
- Telegram Desktop
- QBittorrent
- Transmission
- Remmina (remote desktop)
- Wireshark
- OpenVPN, WireGuard

### Security
- KeePassXC (password manager)
- ClamAV (antivirus)
- UFW/Firewalld (firewall)
- GnuPG (encryption)
- AppArmor

And many more utilities, fonts, and tools!

## Post-Installation

After installing LtnOS, you may want to:

- Update the system: `sudo pacman -Syu`
- Install additional packages: `sudo pacman -S <package-name>`
- Install GNOME Extensions via [extensions.gnome.org](https://extensions.gnome.org/)
- Customize GNOME settings through Settings or GNOME Tweaks
- Install additional GNOME applications: `sudo pacman -S gnome-<app-name>`

## Package Management

LtnOS uses the Arch Linux package manager, pacman:

```bash
# Update system
sudo pacman -Syu

# Install packages
sudo pacman -S package-name

# Remove packages
sudo pacman -R package-name

# Search for packages
pacman -Ss search-term
```

### AUR Support

Access the Arch User Repository (AUR) using helpers like `yay` or `paru`:

```bash
yay -S aur-package-name
```


## Documentation

For more detailed information, please refer to:

- [Arch Linux Wiki](https://wiki.archlinux.org/)
- [LtnOS Documentation](https://ltnproject.github.io/LtnOSDoc) 
## Contributing

Contributions are welcome! If you'd like to contribute to LtnOS:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Support

If you encounter issues or have questions:

- Open an issue on the GitHub repository
- Check the Arch Linux forums for general Arch-related questions

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built on [Arch Linux](https://archlinux.org/)
- Thanks to the Arch Linux community for their excellent documentation and support
- GNOME Desktop Environment
- All the amazing open-source projects included in LtnOS

## Technical Details

- **Base**: Arch Linux
- **Kernel**: Latest stable Linux kernel with headers
- **Init System**: systemd
- **Display Server**: Wayland (with X11/Xorg fallback)
- **Desktop**: GNOME (complete with extras)
- **Display Manager**: GDM
- **Audio**: PipeWire with ALSA/PulseAudio compatibility
- **Bootloader**: GRUB with custom theme
- **Boot Splash**: Plymouth
- **Network**: NetworkManager
- **Firmware**: Intel/AMD microcode, extensive Linux firmware
- **Graphics Drivers**: Mesa, NVIDIA proprietary, AMD, Intel
- **File Systems**: Support for ext4, Btrfs, XFS, F2FS, NTFS, exFAT
- **Package Count**: 1000+ packages from official repositories

## Version History

### 1.0.0 "Nebula" (Current)
- Initial stable release
- Complete GNOME desktop environment
- 150+ pre-installed applications
- Custom GRUB and Plymouth themes
- Full hardware support
- Developer tools included
- Gaming and multimedia ready

## Roadmap

### Version 1.1 (Planned)
- [ ] Live USB persistence option
- [ ] Custom Calamares installer with LtnOS branding
- [ ] Pre-configured GNOME extensions pack
- [ ] Additional Plymouth themes
- [ ] Flatpak integration
- [ ] Automatic driver detection and installation
- [ ] LtnOS configuration center

### Version 1.2 (Future)
- [ ] Custom software repository for LtnOS-specific packages
- [ ] Alternative desktop environment flavors (KDE Plasma, XFCE)
- [ ] Enhanced gaming performance optimizations
- [ ] Cloud sync integration
- [ ] Custom GNOME shell theme

---

**Note**: LtnOS is a custom distribution built with archiso. Always back up your data before installation.
