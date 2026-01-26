#hyprland

Key binds for Hyprland can be set in the Hyprland config file at `.config/hypr/hyprland.conf`

Set "Windows" key as main modifier:
$mainMod = SUPER

Main Key Binds:
bind = $mainMod, Q, exec, $terminal
bind = $mainMod, C, killactive,
bind = $mainMod SHIFT, M, exec, command -v hyprshutdown >/dev/null 2>1 && hyprshutdown || hyprctl dispatch exit
bind = $mainMod, E, exec, $fileManager
bind = $mainMod, R, exec, $menu -show drun
bind = $mainMod SHIFT, R, exec, $menu -show window

Laptop multimedia binds:
bindel = , XF86MonBrightnessUp, exec, brightnessctl -e4 -n2 set 5%+
bindel = , XF86MonBrightnessDown, exec, brightnessctl -e4 -n2 set 5%-

Custom set binds:
bind = $mainMod, f, exec, firefox
bind = $mainMod, d, exec, discord
bind = $mainMod, o, exec, obsidian
bind = $mainMod, s, exec, spotify-launcher 
bind = $mainMod SHIFT, s, exec, pwvucontrol
bind = $mainMod SHIFT, w, exec, killall -SIGUSR2 waybar
bind = $mainMod, b, exec, qutebrowser