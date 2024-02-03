# xrandr_brightness
This polybar script module allows you to adjust the brightness of the screen using the xrandr command and also allows you to activate a light filter

## Dependency
1. xrandr
2. bc
3. polybar
4. nerd font icons

## Example
This Polybar script allows you to control both the brightness of the screen and the blue light filter (night mode) with specific actions: 
1. Left Click: Turn on the blue light filter (night mode).
2. Right-click: Turn off the blue light filter.
3. Mouse Scroll: Allows you to adjust the brightness of the screen, both up and down.

![xrandr_brightness](https://raw.githubusercontent.com/IamJony/semi-nord-theme-bluefish/main/Screenshot_2024-02-03-12-39-11_1366x768.png)
## Module
the script provides the ability to adjust the temperature of the blue light filter within a range of 6500K to 1000K, allowing for further customization and tailoring to each user's individual preferences.

```
[module/xrandr_brightness]
type = custom/text
content = "%{T6}󰃟 "
interval = 1
scroll-up = ~/.config/polybar/xrandr_brightness.sh --up
scroll-down = ~/.config/polybar/xrandr_brightness.sh --down 
; Temperature 6500k - 1000k
click-left= ~/.config/polybar/night_mode.sh 5000 
click-right= ~/.config/polybar/night_mode.sh --off
```
