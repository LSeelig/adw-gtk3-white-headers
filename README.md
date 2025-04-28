<div align="center">
  
# adw-gtk3-white-headers
A soft fork of [adw-gtk3](https://github.com/lassekongo83/adw-gtk3) that restores the white headerbars introduced with Libadwaita 1.4/GNOME 45.

<sup>*White headerbars were [removed](https://github.com/lassekongo83/adw-gtk3/commit/e20a8ed9d295304544e3a74538b324000f933a83) from adw-gtk3 because they can [reduce the legibility of some apps](https://github.com/lassekongo83/adw-gtk3/issues/247). Please do not make any issue reports for this fork in the original repo.*</sup>

</div>

<p align="center">
  <a href="#how-to-use">How To Use</a> •
  <a href="#customization">Customization</a> •
  <a href="#related-projects">Related Projects</a> •
  <a href="#credits">Credits</a>
</p>

<div align="center">

| Light theme (fork) | Light theme (adw-gtk3) | Dark theme (either)|
|:-----------:|:-----------:|:----------:|
| ![adw-gtk3-light](images/preview-wh.png?raw=true) | ![adw-gtk3-light](images/preview-light.png?raw=true) | ![adw-gtk3-dark](images/preview-dark.png?raw=true) |

<sup>*Wallpapers: [here](https://i.imgur.com/kU8D1nV.png) and [here](https://old.reddit.com/r/wallpaper/comments/1f8hlcr/wavy_mountain_3840x2160/)*</sup>

</div>

<div align="center">
  
## How to Use

</div>

<div align="center">

| Tarball | Repository | Flatpak | Source |
|:---:|:---:|:---:|:---:|
| 📦 [Download](https://github.com/lseelig/adw-gtk3-wh/releases/latest)  | ⬇️ [Unavailable](#repositories) | 📦 [See info below](#flatpak) | 🔧 [More information](src/README.md) |

If you download the tarball, then extract the content of the file to: `~/.local/share/themes/`

</div>

### Repositories
Unfortunately, this fork is not packaged in any repositories.

### Flatpak
This fork cannot currently be installed from Flathub, so flatpak applications will not be styled unless you install from the [tarball](https://github.com/LSeelig/adw-gtk3-white-headers/releases/latest) (or the [source](src/README.md)) to `~/.local/share/themes` and use flatpak override:
```bash
sudo flatpak override --filesystem=xdg-data/themes
```
#### How to activate the theme

<sup>You may want to install this alongside the original theme. That way, if you encounter issues with white headerbars for a specific program, you can switch it to adw-gtk3 by prepending `GTK_THEME=adw-gtk3` to the exec in its desktop entry.</sup>

1. Install `gnome-tweaks` and set the theme under *Appearance > Legacy Applications*. For dark themes, adjust in `gnome-control-center` > *Appearance*.
2. Optional: You can also use `gsettings` to switch themes:

Light theme:
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-wh' && gsettings set org.gnome.desktop.interface color-scheme 'default'
```
Dark theme (identical to adw-gtk3-dark but useful if you use a [toggle](https://gitlab.com/rmnvgr/nightthemeswitcher-gnome-shell-extension)):
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'adw-gtk3-wh-dark' && gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'
```
Revert to default:
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'Adwaita' && gsettings set org.gnome.desktop.interface color-scheme 'default'
```

<div align="center">

## Customization
Adw-gtk3 and libadwaita can be customized with GTK named colors, but this fork is untested. See [adw-colors](https://github.com/lassekongo83/adw-colors) for more info.

<sub>If you want to change the accent color for most applications in GNOME 47 or later, you can use a small CLI program [accent-color-change](https://github.com/lassekongo83/adw-colors/tree/main/accent-color-change).</sub>

![adw-gtk3-customized](images/preview-customized.png?raw=true)

<sup>*Wallpaper: [here](https://i.imgur.com/ZbyNlmh.png)* | *Customization: [Peninsula-dark](thttps://github.com/lassekongo83/adw-colors/tree/main/themes/Peninsula-dark)*</sup>

</div>

<div align="center">

## Related Projects

</div>

<div align="center">

| Software | URL |
|:---|:---|
| Adw-gtk3 (original) | https://github.com/lassekongo83/adw-gtk3 |
| GTK2 | https://github.com/eylles/adw-gtk2-colorizer |
| Gimp 3 | https://github.com/dp0sk/adw-gimp3 |
| Kvantum | https://github.com/GabePoel/KvLibadwaita |
| Firefox | https://github.com/rafaelmardojai/firefox-gnome-theme |
| Thunderbird | https://github.com/rafaelmardojai/thunderbird-gnome-theme |
| Steam | https://github.com/tkashkin/Adwaita-for-Steam |
| VSCode | https://github.com/piousdeer/vscode-adwaita |
| Discord | https://github.com/GeopJr/DNOME |
| Obsidian | https://github.com/birneee/obsidian-adwaita-theme |
| xfwm4 | https://github.com/FabianOvrWrt/adw-xfwm4 |

</div>

<div align="center">

## Credits

</div>

- Libadwaita source: https://gitlab.gnome.org/GNOME/libadwaita
- Adw-gtk3 contributors: https://github.com/lassekongo83/adw-gtk3/graphs/contributors
- Adw-gtk3-white-headers contributors: https://github.com/lseelig/adw-gtk3-white-headers/contributors

