# LXQt-and-Sway!

This is a guide on how to get LXQt/LXQt components (such as the panel) working with Sway.  
If you use another wayland compositor, you're out of luck in this guide for getting it to dock on an edge of your screen, not having windows overlap it, etc.  
You are (probably) in luck if you just want it to quit segfaulting, get it visible on your screen, etc. (at least with wlroots based compositors, no promises otherwise)

### What Will work (as of LXQt 1.0)  
* Application Menu (panel)  
* Directory Menu (panel)  
* Sensors (panel)  
* Spacer (panel)
* Volume (panel) (tested with alsa & pipewire-alsa)
* World Clock (panel)
* Quick Launch**???** (panel) (seems functional, can't test, please confirm)
* Backlight (panel & settings)  

### What *Won't* work (as of LXQt 1.0)  
* Task Manager (panel) (just unfunctional)  
* Desktop Switcher (panel) (**causes segfault**)  
* Keyboard State Indicator**???** (panel) (just unfunctional) (possibly something on my side, please confirm)

See also: LXQt's wayland TODO on their wiki here: <https://github.com/lxqt/lxqt/wiki/TODO-for-Wayland>
## How to: the Panel
