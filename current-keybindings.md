# Current Hyprland Keybindings

This document lists all keybindings currently active in the Hyprland configuration, sourced from both Omarchy defaults and custom configurations.

## Window Management (tiling.conf)

### Basic Window Control
- `SUPER + W` - Close active window
- `SUPER + V` - Toggle floating mode
- `SHIFT + F11` - Toggle fullscreen

### Window Focus Movement
- `SUPER + ←/→/↑/↓` - Move focus with arrow keys

### Window Swapping
- `SUPER + SHIFT + ←/→/↑/↓` - Swap active window with adjacent window

### Window Resizing
- `SUPER + -` - Resize active window (width -100)
- `SUPER + =` - Resize active window (width +100)
- `SUPER + SHIFT + -` - Resize active window (height -100)
- `SUPER + SHIFT + =` - Resize active window (height +100)

### Tiling Control
- `SUPER + J` - Toggle split direction (dwindle)
- `SUPER + P` - Toggle pseudo-tiling (dwindle)

## Workspace Management (tiling.conf)

### Switch to Workspace
- `SUPER + 1-9,0` - Switch to workspace 1-10

### Move Window to Workspace
- `SUPER + SHIFT + 1-9,0` - Move active window to workspace 1-10

### Workspace Navigation
- `SUPER + Mouse Scroll` - Scroll through workspaces
- `ALT + Tab` - Cycle through applications on active workspace

## Mouse Controls (tiling.conf)
- `SUPER + Left Mouse` - Move window
- `SUPER + Right Mouse` - Resize window

## System Utilities (utilities.conf)

### Application Launcher
- `SUPER + Space` - Launch walker (app launcher)
- `SUPER + K` - Show keybindings menu

### Aesthetics & UI
- `SUPER + SHIFT + Space` - Reload waybar
- `SUPER + CTRL + Space` - Next background theme
- `SUPER + SHIFT + CTRL + Space` - Theme menu

### Notifications
- `SUPER + ,` - Dismiss current notification
- `SUPER + SHIFT + ,` - Dismiss all notifications
- `SUPER + CTRL + ,` - Toggle do-not-disturb mode

### Power & System
- `SUPER + Escape` - Power menu (lock, suspend, restart, shutdown)
- `SUPER + CTRL + I` - Toggle idle mode

### Screenshots & Recording
- `Print` - Take screenshot
- `SHIFT + Print` - Screenshot active window
- `CTRL + Print` - Screenshot current output
- `ALT + Print` - Start screen recording
- `CTRL + ALT + Print` - Record current output
- `SUPER + Print` - Color picker

### Screensaver
- `SUPER + ALT + Space` - Launch screensaver

### Apple Display Control
- `CTRL + F1` - Decrease Apple display brightness
- `CTRL + F2` - Increase Apple display brightness
- `SHIFT + CTRL + F2` - Max Apple display brightness

## Media Controls (media.conf)

### Volume Control
- `XF86AudioRaiseVolume` - Increase volume
- `XF86AudioLowerVolume` - Decrease volume
- `XF86AudioMute` - Toggle volume mute
- `XF86AudioMicMute` - Toggle microphone mute

### Brightness Control
- `XF86MonBrightnessUp` - Increase screen brightness
- `XF86MonBrightnessDown` - Decrease screen brightness

### Media Player Control
- `XF86AudioNext` - Next track
- `XF86AudioPrev` - Previous track
- `XF86AudioPlay/Pause` - Play/pause media

## Custom Applications (keybinds.conf)

### Core Applications
- `SUPER + Return` - Terminal (alacritty)
- `SUPER + F` - File manager (nautilus)
- `SUPER + B` - Browser (Chrome default profile)
- `SUPER + SHIFT + B` - Work browser (Chrome work profile)

### Development Tools
- `SUPER + Z` - Zed editor
- `SUPER + E` - Terminal Emacs
- `SUPER + T` - System monitor (btop)
- `SUPER + D` - Docker manager (lazydocker)

### Communication & Productivity
- `SUPER + M` - Spotify
- `SUPER + SHIFT + Z` - Zoom
- `SUPER + SHIFT + G` - Signal
- `SUPER + /` - 1Password

### Web Applications
- `SUPER + A` - ChatGPT
- `SUPER + G` - Gemini
- `SUPER + C` - Google Chat
- `SUPER + SHIFT + C` - Google Calendar
- `SUPER + Y` - YouTube
- `SUPER + X` - X (Twitter)
- `SUPER + SHIFT + X` - X Compose

## Key Conflicts & Notes

### Conflicting Keys
- `SUPER + G` - Used for both Gemini (custom) and would conflict with navigation in README design
- `SUPER + F` - Used for file manager (custom) vs fullscreen (README design)
- `SUPER + Space` - Used for app launcher (omarchy) vs toggle floating (README design)

### Missing from README Design
- No vim-style navigation (H, J, K, L)
- No submap modes for grouped actions
- No `SUPER + Q` for kill active (uses `SUPER + W` instead)