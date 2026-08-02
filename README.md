# APT Repository for DrHelius Emulators

This is the official APT repository (PPA) for [DrHelius](https://github.com/drhelius) emulators, served via GitHub Pages.

## Available Emulators

| Emulator | System | Install Command |
|----------|--------|-----------------|
| [Gearboy](https://github.com/drhelius/Gearboy) | Game Boy / Game Boy Color / Super Game Boy | `sudo apt install gearboy` |
| [Gearsystem](https://github.com/drhelius/Gearsystem) | Sega Master System / Game Gear / SG-1000 | `sudo apt install gearsystem` |
| [Gearcoleco](https://github.com/drhelius/Gearcoleco) | ColecoVision | `sudo apt install gearcoleco` |
| [Geargrafx](https://github.com/drhelius/Geargrafx) | TurboGrafx-16 / PC Engine / SuperGrafx / CD-ROM² | `sudo apt install geargrafx` |
| [Gearlynx](https://github.com/drhelius/Gearlynx) | Atari Lynx | `sudo apt install gearlynx` |
| [Geartowns](https://github.com/drhelius/Geartowns) | FM Towns | `sudo apt install geartowns` |

## Installation

First, add the GPG key and repository:

```bash
curl -fsSL https://drhelius.github.io/ppa-geardome/geardome-ppa.gpg | \
  sudo tee /usr/share/keyrings/geardome-archive-keyring.gpg > /dev/null

echo "deb [arch=amd64,arm64 signed-by=/usr/share/keyrings/geardome-archive-keyring.gpg] \
  https://drhelius.github.io/ppa-geardome resolute main" | \
  sudo tee /etc/apt/sources.list.d/geardome.list
```

> **Note:** Replace `resolute` with your Ubuntu codename: `resolute` (26.04), `noble` (24.04), or `jammy` (22.04).
> Jammy packages are available for amd64 only.

Then install any emulator:

```bash
sudo apt update
sudo apt install gearboy
sudo apt install gearsystem
sudo apt install gearcoleco
sudo apt install geargrafx
sudo apt install gearlynx
sudo apt install geartowns
```

## Updating

To update all emulators to their latest versions:

```bash
sudo apt update && sudo apt upgrade
```

Or update a specific emulator:

```bash
sudo apt update && sudo apt install --only-upgrade geargrafx
```

## Uninstallation

```bash
sudo apt remove geargrafx
```

To remove the repository:

```bash
sudo rm /etc/apt/sources.list.d/geardome.list
sudo rm /usr/share/keyrings/geardome-archive-keyring.gpg
```

## License

This repository is provided under the GNU GPL v3 license.
