<div align="center">

# adw-gtk3-white-headers
A soft fork of [adw-gtk3](https://github.com/lassekongo83/adw-gtk3) that restores the white headerbars introduced with Libadwaita 1.4/GNOME 45.

<sup>*White headerbars were [removed](https://github.com/lassekongo83/adw-gtk3/commit/e20a8ed9d295304544e3a74538b324000f933a83) from adw-gtk3 because they can [reduce the legibility of some apps](https://github.com/lassekongo83/adw-gtk3/issues/247). Please do not make any issue reports for this fork in the original repo.*</sup>

| Light theme (adw-gtk3) | Light theme (fork) | Dark theme |
|:----------------------:|:------------------:|:----------:|
| ![adw-gtk3-light](preview-light.png?raw=true) | ![adw-gtk3-wh](preview-wh.png?raw=true) | ![adw-gtk3-dark](preview-dark.png?raw=true) |

<sup>*Also Used: [Rounded Window Corners](https://github.com/yilozt/rounded-window-corners) and [Night Theme Switcher](https://extensions.gnome.org/extension/2236/night-theme-switcher/)*</sup>

</div>

<div align="center">

## How to install

</div>

**Note:** You may want to install this alongside the original theme. That way, if you encounter issues with white headerbars for a specific program, you can switch it to adw-gtk3 by prepending `GTK_THEME=adw-gtk3` to its exec.

### Tarball
1. Go to the [releases](https://github.com/lseelig/adw-gtk3-white-headers/releases) section and download the latest `tar.xz` file.
2. Extract the file to `~/.themes/` (recommended), `~/.local/share/themes/`, (or `/usr/share/themes` if you want to install it for all users).

**Note:** Do not extract it to multiple locations. Only use one path. If you use flatpak applications, you **MUST** extract it to `~/.themes/`.

3. If you use flatpak applications, you will have to give flatpaks access to the theme. From a terminal, run as root:
```
flatpak override --filesystem=~/.themes:ro
```

**Note:** Both the fork and the original project have a dark variant. They should be identical, as the white headerbars only appear in light mode, but I packaged a dark theme anyways so it will toggle correctly when using recent versions of GNOME or an auto-switch extension.

You can then enable adw-gtk3 in the application `gnome-tweaks`. (Some applications may require a relog.)

Alternatively you can set the theme with your terminal:

Change the theme to the light variant:
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-wh' && gsettings set org.gnome.desktop.interface color-scheme 'default'
```
Change the theme to the dark variant:
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-wh-dark' && gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'
```
Revert to GNOME's default theme:
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'Adwaita' && gsettings set org.gnome.desktop.interface color-scheme 'default'
```

### Other installation options
This is a small fork, so there are no distro packages nor a flatpak, though as detailed above, the theme will still apply to flatpak. If you want updates from your distro's package manager, you will need to use the original project.

### Installation from source
This will install the latest version from the main branch. Use this installation method if you want to contribute and help testing the theme.

See [CONTRIBUTING.md](https://github.com/lseelig/adw-gtk3-white-headers/blob/main/CONTRIBUTING.md) for the instructions.

<div align="center">

## Customizing
If you want to change your accent color for most applications in GNOME 47 or later, then you can use the small cli program [accent-color-change](https://github.com/lassekongo83/adw-colors/tree/main/accent-color-change).

![adw-gtk3-customized](preview-customized.png?raw=true)

<sup>*Wallpaper: [here](https://i.imgur.com/ZbyNlmh.png) | Customization: [Peninsula-dark](https://github.com/lassekongo83/adw-colors/blob/main/themes/Peninsula-dark/gtk.css)*</sup>

</div>

Adw-gtk3 and libadwaita can be customized with GTK named colors. See [adw-colors](https://github.com/lassekongo83/adw-colors) for more info.

Note: GTK3 doesn't support the accent color feature introduced in GNOME 47. Only libadwaita does.

<div align="center">

## For more consistency

</div>

- **GTK4:** [Info on how to extract libadwaita from source.](https://github.com/lassekongo83/adw-gtk3/blob/main/gtk4.md)
- **GTK2:** https://github.com/eylles/adw-gtk2-colorizer
- **Kvantum:** https://github.com/GabePoel/KvLibadwaita
- **Firefox:** https://github.com/rafaelmardojai/firefox-gnome-theme
- **Steam:** https://github.com/tkashkin/Adwaita-for-Steam
- **VSCode:** https://github.com/piousdeer/vscode-adwaita
- **Discord:** https://github.com/GeopJr/DNOME
- **Obsidian:** https://github.com/birneee/obsidian-adwaita-theme
- **xfwm4:** https://github.com/FabianOvrWrt/adw-xfwm4
<div align="center">

>>>>>>> upstream/main
## How to uninstall the theme(s)

</div>

- For a local installation in `~/.themes`: `rm -r ~/.themes/adw-gtk3-wh*`
- For a local installation in `~/.local/share/themes`: `rm -r ~/.local/share/themes/adw-gtk3-wh*`
- For a global installation: `sudo rm -r /usr/share/themes/adw-gtk3-wh*`

<div align="center">

## Credits

</div>

- Libadwaita source: https://gitlab.gnome.org/GNOME/libadwaita
- Adw-gtk3 contributors: https://github.com/lassekongo83/adw-gtk3/graphs/contributors
- Adw-gtk3-white-headers contributors: https://github.com/lseelig/adw-gtk3-white-headers/contributors
