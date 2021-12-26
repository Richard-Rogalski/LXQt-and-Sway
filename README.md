# LXQt-and-Sway!

This is a guide on how to get LXQt/LXQt components (such as the panel) working with Sway.  
If you aren't using Sway but are using another wlroots based compositor (Wayfire, KwinFT, etc) what does and doesn't function should be the same, but you're on your own trying to get it to behave properly. 
I have not tested wayland compositors other than wlroots based ones, but I wouldn't expect too much to be different. 

### What Will work (as of LXQt 1.0)  
* Notifications  
* Application Menu (panel)  
* Directory Menu (panel)  
* Sensors (panel)  
* Spacer (panel)
* Volume (panel) (tested with alsa & pipewire-alsa)
* World Clock (panel)
* Quick Launch **???** (panel) (seems functional, can't test, please confirm)
* Backlight/Brightness (panel & settings)  
* File Associations (settings)
* Appearance - Cursor (settings) (*probably wlroots only*)  

### What *Won't* work (as of LXQt 1.0)  
* Task Manager (panel) (just unfunctional)  
* Desktop Switcher (panel) (**causes segfault**)  
* Keyboard State Indicator **???** (panel) (just unfunctional) (possibly something on my side, please confirm)  
* Monitor Settings (settings) (crashes or doesn't open)  
* Keyboard and Mouse (settings) (doesn't open)

See also: LXQt's wayland TODO on their wiki here: <https://github.com/lxqt/lxqt/wiki/TODO-for-Wayland>
## How to: the Panel
To get the panel working, install lxqt-panel and make sure you **don't have the desktop switcher widget on the bar.**
Then, add these lines to your Sway config file:  
```
## LXQt-panel config
gaps bottom 32
# This is so the bar doesn't partially cover tiled windows
exec --no-startup-id lxqt-panel
no_focus [app_id="lxqt-panel"]
for_window [app_id="lxqt-panel"] floating enable, sticky enable, border none, move down 550 px
# You can use ppt (percantage point) instead of px (pixels). 550px seems to work for a 1080p monitor with a 32px high bar
```
*note: the panel might be 100% invisible by default. try finding it and right clicking it and change its theme*

## How to: Notifications
To get notifications working, install lxqt-notificationd and add the following to your Sway config file:  
```
## LXQt-notificationd config
exec --no-startup-id lxqt-notificationd
no_focus [app_id="lxqt-notificationd"]
for_window [app_id="lxqt-notificationd"] floating enable, sticky enable, border none, move down 400 px, move right 700 px
```
