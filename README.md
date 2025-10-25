# ROBLOX Script Hub v2.1.2

A feature-rich, mobile-friendly script hub for ROBLOX with visibility controls, UI management, and spectator functionality.

![Version](https://img.shields.io/badge/version-2.1.2-blue.svg)
![Platform](https://img.shields.io/badge/platform-ROBLOX-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

### 👁️ Visibility Controls
- **Hide Title** - Hide player nametags and overhead displays
- **Hide Players** - Make other players invisible (including their titles and displays)

### 📱 Interface Management
- **Hide All UI** - Hide game UI elements while preserving:
  - Player List (Leaderboard)
  - Chat system
  - Emotes menu
  - Healthbar and backpack are hidden

### 🎥 Camera Features
- **Spectator Mode** - Advanced spectator system with:
  - Smooth player-to-player navigation
  - Arrow controls for switching targets
  - Player info display (DisplayName & Username)
  - Preserved leaderboard visibility
  - Auto-cleanup when players leave
  - Automatic UI hiding during spectation

## 🚀 Installation

1. Copy the entire script from `script.lua`
2. Paste it into your ROBLOX executor
3. Execute the script
4. Click the hamburger menu button (top-right corner) to open the hub

## 📱 Platform Support

- ✅ **PC/Desktop** - Full functionality with optimized UI sizing
- ✅ **Mobile** - Touch-optimized interface with adjusted button sizes
- ✅ **Tablet** - Adaptive layout for various screen sizes

## 🎮 Usage

### Opening the Menu
- Click/tap the **hamburger button** (☰) in the top-right corner
- The menu will smoothly expand with all available categories

### Navigating Categories
- Click on any category header to expand/collapse it
- Only one category can be expanded at a time for cleaner UI
- Categories include:
  - 👁️ Visibility
  - 📱 Interface  
  - 🎥 Camera

### Toggling Features
- Each feature has a toggle switch
- **Enabled** = Cyan indicator with "● Enabled" status
- **Disabled** = Gray indicator with "● Disabled" status
- Changes apply instantly

### Spectator Mode Controls
When spectator mode is active:
- **◀ Left Arrow** - Previous player
- **▶ Right Arrow** - Next player
- **Info Display** - Shows current spectated player's name
- **Auto-hide** - UI and player titles are automatically hidden
- **Exit** - Toggle spectator mode off to return to normal view

## 🔧 Technical Details

### Services Used
```lua
- Players
- UserInputService
- TweenService
- RunService
- StarterGui
```

### UI Framework
- **ScreenGui** with high DisplayOrder (999999)
- **ResetOnSpawn** disabled for persistence
- **Adaptive sizing** based on platform detection
- **Smooth animations** using TweenService

### Color Scheme
```lua
Primary: RGB(88, 101, 242)    - Discord Blurple
Secondary: RGB(114, 137, 218)  - Light Blurple
Background: RGB(25, 28, 33)    - Dark Gray
Accent: RGB(88, 201, 242)      - Cyan
```

## 📝 Changelog

### v2.1.2 (Current)
- ✅ Enhanced Hide All UI to preserve PlayerList, Chat, and Emotes
- ✅ Only hides Health and Backpack CoreGui elements
- ✅ Improved spectator mode with leaderboard visibility
- ✅ Better player GUI detection and hiding
- ✅ Added leaderboard exclusion checks

### v2.1.1
- Enhanced Hide Players to include titles
- Improved mobile responsiveness
- Bug fixes for UI scaling

### v2.1.0
- Added Spectator Mode
- Category-based organization
- Improved animations

### v2.0.0
- Complete UI overhaul
- Mobile support
- Toggle button redesign

## ⚠️ Known Limitations

- Spectator mode cannot spectate players without a character
- Some custom UI elements may not be detected by Hide All UI
- Mobile performance may vary on low-end devices

## 🛠️ Customization

### Changing Colors
Edit the `COLORS` table:
```lua
local COLORS = {
    primary = Color3.fromRGB(88, 101, 242),
    secondary = Color3.fromRGB(114, 137, 218),
    -- Add your custom colors here
}
```

### Adjusting Sizes
Modify the `SIZES` table:
```lua
local SIZES = {
    toggleBtn = isMobile and 25 or 30,
    menuWidth = isMobile and 135 or 200,
    -- Customize dimensions here
}
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is licensed under the MIT License - see below:

```
MIT License

Copyright (c) 2024 ItoRenz00

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👤 Author

**ItoRenz00**
- GitHub: [@ItoRenz](https://github.com/ItoRenz)

## 🌟 Support

If you find this script helpful, please:
- ⭐ Star this repository
- 🐛 Report any bugs you find
- 💡 Share your feature ideas

---

## 📋 Commit Message Template

```
feat: v2.1.2 - Enhanced UI hiding with leaderboard preservation

Major Changes:
- Improved Hide All UI to exclude PlayerList, Chat, and Emotes
- Now only hides Health and Backpack CoreGui elements
- Enhanced spectator mode with visible leaderboard
- Better player GUI detection for hiding overhead displays

Technical Improvements:
- Added isLeaderboardGui() function for smart UI detection
- Improved hidePlayerGui() with better scope handling
- Enhanced cleanup system for spectator mode
- Fixed UI restoration on spectator exit

Bug Fixes:
- Fixed issue where chat/emotes were hidden unnecessarily
- Resolved leaderboard hiding during spectator mode
- Improved memory cleanup on script destruction

Platform Support:
- Maintained full mobile/desktop compatibility
- Optimized UI sizing for both platforms
- Improved touch responsiveness on mobile

This update focuses on preserving essential UI elements (leaderboard, 
chat, emotes) while hiding non-essential elements, providing a cleaner
spectating experience without losing important game information.
```

---

**Made with ❤️ for the ROBLOX community**
