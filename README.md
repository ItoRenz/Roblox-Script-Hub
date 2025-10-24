# 🎮 Roblox Script Hub - Compact Layout

A lightweight, responsive script hub for Roblox with a modern hamburger menu interface and essential utility features.

## 👤 Author
**ItoRenz00**

## ✨ Features

- **👁 Hide Title** - Hide player name displays and billboards
- **👤 Hide Players** - Make other players invisible (transparency + GUI hiding)
- **📱 Hide All UI** - Toggle visibility of all ScreenGui elements
- **🍔 Hamburger Menu** - Smooth animated toggle button with X transformation
- **📱 Responsive Design** - Optimized layouts for both mobile and PC
- **🎨 Modern UI** - Discord-inspired color scheme with smooth animations
- **🛡️ Error Protection** - Full pcall protection on all connections
- **🧹 Auto Cleanup** - Automatic cleanup system on script removal

## 📦 Installation

### Method 1: Roblox Studio
1. Open Roblox Studio
2. Insert a **LocalScript** into:
   - `StarterGui` (recommended), or
   - `StarterPlayer > StarterPlayerScripts`
3. Copy and paste the script code
4. Save and test in Play mode

### Method 2: Executor (Client-side)
1. Copy the entire script
2. Paste into your executor
3. Execute the script

## 🎯 Usage

### Opening the Menu
- Click the **hamburger button** (☰) in the top-right corner
- The button animates into an X when the menu is open

### Features Control
Each feature has a toggle switch:
- **Green/Blue** = Enabled ✅
- **Gray** = Disabled ❌

### Closing the Menu
- Click the hamburger button again, or
- Click the **red X button** in the menu header

## 📐 UI Specifications

### Mobile Layout
- Toggle Button: 25x25px
- Position: Top-right (35px from right, 5px from top)
- Menu Panel: 135x140px
- Items: Compact 30px height

### PC Layout
- Toggle Button: 30x30px
- Position: Top-right (37px from right, 10px from top)
- Menu Panel: 200x200px
- Items: Standard 42px height

## 🔧 Technical Details

### Script Structure
```
Script Hub
├── Toggle Button (Hamburger Menu)
├── Menu Panel
│   ├── Header (with close button)
│   ├── ScrollingFrame
│   └── Script Items
└── Script Modules
    ├── Hide Title
    ├── Hide Players
    └── Hide All UI
```

### Key Features
- **Platform Detection**: Automatically detects mobile/PC
- **TweenService**: Smooth animations for all UI elements
- **Connection Management**: Safe connection handling with cleanup
- **Error Handling**: pcall wrapping on all critical operations
- **Memory Management**: Proper cleanup on script removal

## 🎨 Color Scheme

- Primary: `RGB(88, 101, 242)` - Discord Blurple
- Secondary: `RGB(114, 137, 218)` - Light Blurple
- Background: `RGB(25, 28, 33)` - Dark Gray
- Items: `RGB(35, 38, 43)` - Medium Gray
- Accent (Active): `RGB(88, 201, 242)` - Cyan
- Accent (Danger): `RGB(237, 66, 69)` - Red

## 📝 Script Descriptions

### Hide Title
Hides all player name displays including:
- BillboardGui elements
- SurfaceGui on character heads
- TextLabel/TextButton/TextBox in head
- Humanoid display distance settings

### Hide Players
Makes other players completely invisible:
- Sets all BaseParts to full transparency
- Hides Decals and Textures
- Disables ParticleEmitters, Beams, and Trails
- Hides all character GUIs and text elements
- Maintains collision detection off

### Hide All UI
Toggles all ScreenGui elements:
- Hides all GUI except the Script Hub
- Remembers original enabled states
- Restores all UI when disabled

## ⚠️ Important Notes

1. **LocalScript Only**: This script must run as a LocalScript (client-side)
2. **ResetOnSpawn**: Set to false - the GUI persists through respawns
3. **Compatibility**: Works on all Roblox games (universal)
4. **Performance**: Optimized for minimal performance impact
5. **Safety**: All operations wrapped in pcall for error protection

## 🐛 Troubleshooting

### GUI not appearing
- Ensure script is in `StarterGui` or `StarterPlayerScripts`
- Check if it's a LocalScript (not Script)
- Verify no errors in output console

### Features not working
- Make sure you're testing in Play mode
- Check that the game allows LocalScript execution
- Some games may have anti-cheat that blocks certain features

### Mobile controls not working
- The script auto-detects mobile devices
- Try restarting the game if layout seems wrong

## 📄 License

This script is free to use and modify for personal use.

## 🤝 Contributing

Feel free to fork and improve this script! If you make enhancements:
1. Keep the author credit intact
2. Document your changes
3. Test thoroughly on both mobile and PC

## 📞 Support

For issues or questions:
- Check the troubleshooting section
- Review the code comments
- Test in a clean Roblox game first

## 🔄 Version History

### Version 1.0.0
- Initial release
- Three core features (Hide Title, Hide Players, Hide All UI)
- Responsive mobile/PC layout
- Hamburger menu with animations
- Full error protection and cleanup system

---

**Made with ❤️ by ItoRenz00**

*Last Updated: 2025*
