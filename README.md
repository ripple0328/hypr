# Hyprland Keybinding Configuration

This document outlines a logical and ergonomic keybinding scheme for Hyprland. It is based on two principles:
1.  **Core Layer:** The most frequent actions have simple, direct keybindings (`SUPER + Key`).
2.  **Prefix Layers:** Related, less-frequent actions are grouped into categories using `submap` modes (e.g., `SUPER + R` to enter "Resize Mode").

## `hyprland.conf` Keybindings

Copy and paste the following code into your `~/.config/hypr/hyprland.conf`. Remember to adjust applications (like `kitty` and `wofi`) and key choices to your personal preference.

```ini
########################################################################################
#                          HYPRLAND KEYBINDING CONFIGURATION                           #
########################################################################################

# Set the main modifier key (SUPER is the "Windows" key)
$mainMod = SUPER

# --------------------------------------------------------------------------------------
# -- CORE LAYER: High-frequency actions
# --------------------------------------------------------------------------------------

# Launch essential applications
bind = $mainMod, RETURN, exec, kitty
bind = $mainMod, D, exec, wofi --show drun

# Kill the active window
bind = $mainMod, Q, killactive,

# Toggle window state
bind = $mainMod, SPACE, togglefloating,
bind = $mainMod, F, fullscreen,

# --------------------------------------------------------------------------------------
# -- NAVIGATION: Moving focus and workspaces
# --------------------------------------------------------------------------------------

# Move focus using Vim-style keys
bind = $mainMod, H, movefocus, l
bind = $mainMod, L, movefocus, r
bind = $mainMod, K, movefocus, u
bind = $mainMod, J, movefocus, d

# Switch to a workspace
bind = $mainMod, 1, workspace, 1
bind = $mainMod, 2, workspace, 2
bind = $mainMod, 3, workspace, 3
bind = $mainMod, 4, workspace, 4
bind = $mainMod, 5, workspace, 5
bind = $mainMod, 6, workspace, 6
bind = $mainMod, 7, workspace, 7
bind = $mainMod, 8, workspace, 8
bind = $mainMod, 9, workspace, 9
bind = $mainMod, 0, workspace, 10

# Move the active window to a workspace
bind = $mainMod SHIFT, 1, movetoworkspace, 1
bind = $mainMod SHIFT, 2, movetoworkspace, 2
bind = $mainMod SHIFT, 3, movetoworkspace, 3
bind = $mainMod SHIFT, 4, movetoworkspace, 4
bind = $mainMod SHIFT, 5, movetoworkspace, 5
bind = $mainMod SHIFT, 6, movetoworkspace, 6
bind = $mainMod SHIFT, 7, movetoworkspace, 7
bind = $mainMod SHIFT, 8, movetoworkspace, 8
bind = $mainMod SHIFT, 9, movetoworkspace, 9
bind = $mainMod SHIFT, 0, movetoworkspace, 10

# --------------------------------------------------------------------------------------
# -- PREFIX LAYERS: Using submaps for categorical actions
# --------------------------------------------------------------------------------------

# --- Resize Mode ---
# Define the submap
submap = resize
# Binds for resizing windows. 'binde' allows for repeated execution.
binde = , L, resizeatleast, 10 0
binde = , H, resizeatleast, -10 0
binde = , K, resizeatleast, 0 -10
binde = , J, resizeatleast, 0 10
# Exit the submap with Escape
bind = , escape, submap, reset
# End submap definition
submap = reset
# Bind a key to enter the resize submap
bind = $mainMod, R, submap, resize


# --- System Control Mode ---
# Define the submap
submap = system
# Binds for system actions
bind = , L, exec, swaylock
bind = , E, exit,
bind = , S, exec, systemctl poweroff
bind = , R, exec, systemctl reboot
# Exit the submap with Escape
bind = , escape, submap, reset
# End submap definition
submap = reset
# Bind a key to enter the system submap
bind = $mainMod, X, submap, system


# --- Layout Mode ---
# Define the submap
submap = layout
# Binds for changing layout properties
bind = , S, togglesplit, # Toggle between vertical and horizontal split
bind = , P, pseudo, # Toggle pseudotiling for the active window
# Exit the submap with Escape
bind = , escape, submap, reset
# End submap definition
submap = reset
# Bind a key to enter the layout submap
bind = $mainMod, L, submap, layout
