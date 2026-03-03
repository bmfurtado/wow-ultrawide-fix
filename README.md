# Ultrawide Fix for World of Warcraft

**Ultrawide Fix** is a World of Warcraft addon designed specifically to improve the user experience for players using extremely wide monitors (such as 32:9 displays like the Samsung Odyssey G9). 

## Rationale
By default, World of Warcraft scales its User Interface relatively to the edges of the physical screen. On standard 16:9 or even 21:9 monitors, this is perfectly fine. However, on "super ultrawide" 32:9 screens, this behavior pushes essential UI elements—like the minimap, chat boxes, and default action bars—so incredibly far apart that it becomes uncomfortable to play. Constantly turning your head or shifting your eyes to the extreme edges of a 49-inch display during gameplay can cause neck strain and slow down response times.

**Ultrawide Fix** solves this by restricting the internal bounds of the UI (the `UIParent` frame) horizontally and/or vertically to a custom pixel size. This allows you to place your UI elements within a more narrow, comfortable, and centered slice of the monitor, while keeping the full panoramic 32:9 view for the 3D game world itself!

## Features
* **Custom UI Bounds**: Explicitly set the maximum allowed width and height for your interface in pixels.
* **Resolution-Based Profiles**: Your settings automatically save into different profiles based on the physical screen resolution of your display. If you swap back and forth between a laptop screen and an external Ultrawide, your UI limits will adapt seamlessly!
* **Native Integration**: Options seamlessly integrate into the modern World of Warcraft Options menu (via the new Dragonflight/The War Within Settings API).
* **Live Preview System**: While changing limits via the sliders, a temporary green bordering frame appears onscreen to clearly demonstrate the boundaries of your new UI layout before you even close the menu.

## How it Works
When transitioning into the world or changing UI scaling settings, the addon forces World of Warcraft's `UIParent` canvas size to respect the limitations defined in your Addon settings. Modifying these limits dynamically updates your UI scaling instantly without needing to reload the UI.

# Disclaimer
This addon is a product of pure vibe coding; while it has been tested primarily on Retail and seems to be holding it together, I offer no guarantees that it’s actually "good" or even reliable. Consider this an experimental labor of love rather than a polished professional tool. Use it at your own risk, keep your expectations low, and enjoy the vibes.
