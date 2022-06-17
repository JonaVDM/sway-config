# sway-config

This repo contains everything related to my sway setup. The rest of my dotfiles
can be found [here](https://github.com/JonaVDM/dotfiles).

## Setup

To make use of this config make sure to install the following packages:
- sway
- swaylock
- swayidle
- waybar
- mako
- pulseaudio
- playerctl
- python-gobject
- gtk3
- pavucontrol
- grim
- slurp
- rofi
- xorg-xwayland
- libpulse

Then to link all the directories in place
```bash
ln -s "$(pwd)/mako" ~/.config
ln -s "$(pwd)/rofi" ~/.config
ln -s "$(pwd)/sway" ~/.config
ln -s "$(pwd)/swaylock" ~/.config
ln -s "$(pwd)/waybar" ~/.config
```

## Keybindings

A quick overview from all the keybindings used in the sway config. The 
[h, j, k, l] comes from vim and translates to [left, up, down, right].


| Keybinding                 | Function                                         |
| -------------------------- | ------------------------------------------------ |
| Mod + Enter                | Open terminal                                    |
| Mod + Control + Enter      | Open terminal without tmux                       |
| Mod + Shift + Enter        | Open terminal in floating mode                   |
| Mod + e                    | Open file explorer (Thunar)                      |
| Mod + Shift + e            | Open file explorer (Thunar) in floating mode     |
| Mod + b                    | Open browser (Firefox)                           |
| Mod + Shift + q            | Kill window                                      |
| Mod + Space                | Open app launcher                                |
| Mod + Shift + c            | Reload configuration                             |
| Mod + [h, j, k, l]         | Focus to window in direction                     |
| Mod + Shift + [h, j, k, l] | Move window to direction                         |
| Mod + 1..0                 | Switch to workspace 1..0                         |
| Mod + Shift + 1..0         | Move window to workspace 1..0                    |
| Mod + f                    | Toggle fullscreen on current window              |
| Mod + Shift + Space        | Toggle floating window mode for current screen   |
| Mod + d                    | Toggle focus between floating and tiling windows |
| Mod + a                    | Toggle focus to the parent window                |
| Mod + Shift + Minus        | Move window to scratchpad                        |
| Mod + Minus                | Show application in scratchpad                   |
| Mod + Control + l          | Lock the screen                                  |
| Function mute              | Mute the volume                                  |
| Function volume up         | Volume up                                        |
| Function volume down       | Volume down                                      |
| Function stop              | Stop currently playing                           |
| Function previous          | Play previous                                    |
| Function next              | Play next                                        |
| Function play/pause        | Toggle play/pause                                |
| Mod + Print                | Make a screenshot                                |
| Mod + Shift + Print        | Make a screenshot of selection                   |
| Mod + r                    | Go into resize mode                              |

## Styles for waybar

The styling for waybar is written in scss and needs to be compiled down to
normal css before waybar knows what to do with it.

1. First make sure you have node/npm installed, after which the `sass` packages
can be installed.
```bash
npm i -g sass
```

2. Navigate to the right folder and run the sass compile command.
```
cd ~/.config/waybar
sass --style=compressed --no-source-map style.scss style.css
```
