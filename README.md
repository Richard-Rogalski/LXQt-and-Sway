# LXQt-and-Sway!

This is a guide on how to get LXQt/LXQt components (such as the panel) working with Sway.  
If you use another wayland compositor, you're out of luck in this guide for getting it to dock on an edge of your screen, not having windows overlap it, etc.  
You are (probably) in luck if you just want it to quit segfaulting, get it visible on your screen, etc. (at least with wlroots based compositors, no promises otherwise)

### What Will work (as of LXQt 1.0)  
* Application Menu (panel)  

### What *Won't* work (as of LXQt 1.0)  
* Task manager (panel) (just unfunctional)  
* Desktop switcher (panel) (**causes segfault**)  

## How to: the Panel
