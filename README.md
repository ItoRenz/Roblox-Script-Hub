# 🎮 ROBLOX Script Hub - Compact Layout

A modern, responsive, and feature-rich script hub for ROBLOX with hamburger menu animation and smooth UI interactions.

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-ROBLOX-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

- 🍔 **Animated Hamburger Menu** - Smooth 3-line to X transformation
- 📱 **Mobile & PC Responsive** - Optimized layouts for both platforms
- 🎨 **Modern UI Design** - Discord-inspired color scheme with gradients
- 🔄 **Smooth Animations** - TweenService-powered transitions
- 🛡️ **Full Error Protection** - All connections wrapped in pcall
- 🧹 **Auto Cleanup System** - Proper disposal of connections and GUI
- 👁️ **Hide Player Titles** - Remove BillboardGuis and player names
- 📱 **Hide All UI** - Toggle visibility of all screen GUIs
- ⚡ **Lightweight** - Optimized and compact codebase
- 🎯 **Easy to Use** - One-click toggle switches

## 📊 Specifications

### Mobile 📱
- **Toggle Button:** 25x25px
- **Position:** 60px from top, 35px from right
- **Menu Size:** 135x170px
- **Item Height:** 30px
- **Text Size:** 8-9px

### PC 💻
- **Toggle Button:** 30x30px
- **Position:** 70px from top, 36px from right
- **Menu Size:** 200x280px
- **Item Height:** 42px
- **Text Size:** 11-13px

## 🚀 Installation

### Method 1: Direct Copy (Recommended)

1. Copy the script from the artifact
2. Open ROBLOX Studio
3. Create a new `LocalScript` in:
   - `StarterGui` OR
   - `StarterPlayer → StarterPlayerScripts`
4. Paste the script
5. Save and play!

### Method 2: GitHub

```bash
# Clone the repository
git clone https://github.com/yourusername/roblox-script-hub.git

# Copy the script file to your ROBLOX Studio project
```

## 📖 Usage

### Opening the Menu
Click the hamburger button (☰) in the top-right corner of the screen.

### Available Scripts

#### 👁️ Hide Player Titles
- Hides all BillboardGuis above player heads
- Removes player names and titles
- Automatically applies to new players
- Works with character respawns

#### 📱 Hide All UI
- Toggles visibility of all screen GUIs
- Preserves original states
- Excludes the script hub itself
- Instant toggle on/off

### Toggle Switches
Each script has a smooth toggle switch:
- **Gray** = Disabled ● OFF
- **Cyan** = Enabled ● ON

## 🎨 Color Scheme

```lua
Primary: rgb(88, 101, 242)    -- Discord Blurple
Secondary: rgb(114, 137, 218)  -- Light Blurple
Background: rgb(25, 28, 33)    -- Dark Gray
Item BG: rgb(35, 38, 43)       -- Medium Gray
Accent: rgb(88, 201, 242)      -- Cyan
Close Button: rgb(237, 66, 69) -- Red
```

## 🛠️ Technical Details

### Services Used
- `Players` - Player management
- `UserInputService` - Input detection and mobile check
- `TweenService` - Smooth animations
- `RunService` - Frame updates

### Key Components
- **ScreenGui** - Main container (DisplayOrder: 999999)
- **Toggle Button** - Hamburger menu with gradient
- **Menu Panel** - Collapsible frame with header
- **ScrollingFrame** - Script list container
- **UIListLayout** - Automatic item positioning

### Animations
- **Hamburger to X:** 0.3s Back easing
- **Menu Open/Close:** 0.3s Back/Quad easing
- **Toggle Switches:** 0.25s Quad easing
- **Hover Effects:** 0.15s smooth transitions
- **Breathing Border:** 2s Sine infinite loop

## 🧹 Cleanup System

The script automatically cleans up when:
- Player leaves the game
- GUI is destroyed
- Script is disabled

All connections are properly disconnected to prevent memory leaks.

## 🔒 Error Protection

Every connection and operation is wrapped in `pcall()` to ensure:
- No script errors break the hub
- Graceful failure handling
- Console warnings for debugging

## 🎯 Performance

- **Minimal resource usage** - Only active connections when needed
- **Optimized rendering** - Z-index management
- **Smart detection** - Mobile vs PC automatic detection
- **Memory efficient** - Proper cleanup and disposal

## 📱 Mobile Support

- Larger touch targets (25px minimum)
- Haptic feedback on toggle
- Optimized text sizes
- Touch-friendly spacing
- Responsive positioning

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by modern UI/UX design principles
- Discord color scheme reference
- ROBLOX developer community

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Contact via Discord
- Check the FAQ section

## 🔄 Changelog

### Version 1.0.0 (2025-01-XX)
- ✨ Initial release
- 🍔 Hamburger menu animation
- 📱 Mobile and PC responsive design
- 👁️ Hide Player Titles script
- 📱 Hide All UI script
- 🧹 Auto cleanup system
- 🛡️ Full error protection
- 📏 Compact layout optimization

## 🎮 Game Compatibility

Tested and working on:
- ✅ All ROBLOX games
- ✅ Mobile devices (iOS/Android)
- ✅ PC (Windows/Mac)
- ✅ Console (Xbox)

## ⚠️ Disclaimer

This script is for educational purposes. Use responsibly and follow ROBLOX Terms of Service.

---

**Made with ❤️ for the ROBLOX community**

⭐ Star this repository if you found it helpful!
