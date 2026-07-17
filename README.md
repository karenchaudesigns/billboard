# Dynamic Twitch Billboard

A lightweight, customizable browser-source billboard for OBS that allows streamers and mods to update on-screen text dynamically via Twitch chat.

## Features
- **Auto Text Scaling**: Billboard text automatically scales to fit cleanly within the container dimensions and wraps nicely.
- **OBS Ready**: Intended for use as a browser source in Open Broadcaster Software (OBS).
- **Twitch Integration**: Automatically connects to the broadcaster's Twitch chat to listen for commands.
- **Permission Guard**: Only Broadcasters and Mods can trigger updates.

## Setup
1. Add a **Browser Source** in OBS.
2. Check the "Local file" option and point it to the downloaded `index.html` file OR point it to the hosted Github Pages URL of your fork.
3. Very Important: Add `?channel=your_twitch_channel_name` to the end of the URL (either Local file URL or web URL) to link it to your chat.
   - Local File Example: `file:///path/to/Dynamic-Twitch-Billboard/index.html?channel=shroud`
   - Web Example: `https://your-site.github.io/index.html?channel=shroud`
4. Set the Width and Height in OBS. Ensure "Shutdown source when not visible" is off if you want it to run continuously in the background.

## Commands
*These commands can only be used by the Broadcaster and channel Moderators.*

- `!billboard` - Lists all available commands on the billboard screen.
- `!bbt <text>` - Sets the main text for the billboard. (e.g., `!bbt Thanks for watching!`)
- `!bbs <width>x<height>` - Resizes the billboard to the specified dimensions. (e.g., `!bbs 1200x300`)
- `!bbbg <color>` - Sets the background color of the billboard. Supports hex values with or without the `#` prefix. (e.g., `!bbbg #ff0000` or `!bbbg 000000`)
- `!bboutline <color>` - Sets the outline color of the billboard. Supports hex values. Use `none` to remove the outline. (e.g., `!bboutline #ffffff` or `!bboutline none`)
