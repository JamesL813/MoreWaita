# MoreWaita
An Adwaita styled theme with extra icons for popular apps to complement Gnome Shell's original icons.
The purpose of this theme is to provide a consistent look and feel with Gnome Shell's design.

This theme is built upon the work of Gnome's Adwaita designers, Gnome Circle apps' developers and Papirus theme designers with a touch of tinkering from myself and [@dusansimic](https://github.com/dusansimic) and [@julianfairfax](https://github.com/julianfairfax) here and there. The theme covers the most frequently installed dependency GUI apps that almost nobody uses (like Avahi browsers, QT Designer, Software token, etc.) as well as some of the most popular apps people really do install and use.

The purpose of MoreWaita is to add to Adwaita, not modify it, and to do roughly what Breeze does for KDE. This theme does not override any Adwaita icons, nor any Gnome Circle apps icons, nor icons that generally fit into the Adwaita paradigm (like Transmission GTK). Currently, this theme is way less all-inclusive than many others, but the aim is to be on par with Papirus some day. However, this is (mostly) a one-man hobby effort for now, so suggestions, requests, PRs and contributions are very welcome.

For most icons, especially branded ones, the general idea is to stay as close as possible to the original icons – to the point of using them in full – and giving them the distinct Adwaita 'perspective' and general flatness. One thing this theme deviates from is the Gnome colour palette in brand icons – MoreWaita keeps the brand colours.

This theme is built and tested against vanilla Gnome on Arch Linux. If an icon is in the theme, but is not applying to your app, please open an issue and mention the icon name referenced in your app's `.desktop` file.

## Installation

#### Manual installation
##### Download the theme
`git clone https://github.com/somepaulo/MoreWaita.git`

##### Enter the downloaded folder
`cd Morewaita`

##### Install system-wide (recommended)
`./system-install.sh`  
This copies the whole theme folder without the build files into `/usr/share/icons/`. You will be prompted for your password.

##### Install for local user
`./local-install.sh`  
This copies the whole theme folder without the build files into `~/.local/share/icons/`.

##### Update
Use the same steps as for installation.

##### Uninstall
Simply chose another theme and then delete the entire `MoreWaita` folder from either `/usr/share/icons/` or `~/.local/share/icons/` depending on your installation choice above. 

#### Arch Linux
[AUR package (versioned)](https://aur.archlinux.org/packages/morewaita)

[AUR package (git)](https://aur.archlinux.org/packages/morewaita-git)

[Julian's repository](https://gitlab.com/julianfairfax/package-repo#how-to-add-repository-for-arch-based-linux-distributions)

#### Fedora Linux
[COPR repository](https://copr.fedorainfracloud.org/coprs/dusansimic/themes)

The package name is `morewaita-icon-theme`.

#### Ubuntu/Debian Linux

[Julian's repository](https://gitlab.com/julianfairfax/package-repo#how-to-add-repository-for-debian-based-linux-distributions)

## Activation
Either use the `Tweaks` app to choose and activate the icon theme or run the following command:

`gsettings set org.gnome.desktop.interface icon-theme 'MoreWaita'`

## Using custom folder icons
1. Open Files (Nautilus).
2. Find the folder you wish to change the icon for.
3. Right click on the folder.
4. Click on `Properties`.
5. Click on the folder image.
6. Navigate to the MoreWaita installation folder and into the `places` subfolder (typically `/usr/share/icons/MoreWaita/places/scalable/`).
7. Select the icon you wish to use.
8. Click `Open`.
9. Follow the same procedure to revert the icon. Just click `Revert` instead of selecting a new icon in step 7.
![change_folder_icon](https://github.com/somepaulo/MoreWaita/assets/15643750/05e88cbc-3c77-4e1b-a8bd-3e15b84972fa)

## Troubleshooting

#### Theme doesn't apply
If the theme doesn't apply try the following command:

##### For system-wide installation
`sudo gtk-update-icon-cache -f -t /usr/share/icons/MoreWaita && xdg-desktop-menu forceupdate`

##### For local installation
`gtk-update-icon-cache -f -t ~/.local/share/icons/MoreWaita && xdg-desktop-menu forceupdate`

#### Some apps don't get themed
If the theme applies, but a particular app doesn't get themed (and its icon is in MoreWaita), check its respective `.desktop` file. Some apps have icon paths hardcoded into their `.desktop` file or have a different icon name set there or no icon set at all. This can differ between distros. If you happen to have such apps, you'll need to copy their `.desktop` files into `~/.local/share/applications` and modify them there providing the correct icon name. Alternatively, use a menu editor like `MenuLibre` or `Alacarte`.  
If your app's `.desktop` file references an icon name not present in Moreaita's `apps/scalable` folder, please report it in an issue providing the icon name from your system. 

## The icons
![MoreWaita](https://github.com/somepaulo/MoreWaita/assets/15643750/6048eca1-d0e4-4e04-8a5c-7c1eee409998)
