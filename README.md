# 🛠️ ROBLOX Script Hub v2.2.0

A modern, feature-rich script hub for ROBLOX with a clean UI and powerful utilities. Designed for both PC and Mobile platforms.

![Version](https://img.shields.io/badge/version-2.2.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-ROBLOX-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

## ✨ Features

### 👁️ Visibility
- **Hide Title** - Hide all player nametags and displays
- **Hide Players** - Make other players invisible (characters + titles)

### 📱 Interface
- **Hide All UI** - Hide game UI elements while keeping leaderboard, chat, and emotes menu visible

### 🎥 Camera
- **Spectator Mode** - Spectate other players with navigation controls
  - Keep leaderboard visible while spectating
  - Navigate between players with arrow buttons
  - Automatic player list updates

### 🔄 Reset
- **Reset to Base** - Instant teleport to basecamp with checkpoint reset
  - Automatic basecamp detection
  - Physics reset
  - Health restoration
  - Server-side checkpoint reset support

## 📦 Installation

### Client Script
1. Open your ROBLOX game in Studio
2. Navigate to `StarterPlayer` > `StarterPlayerScripts`
3. Create a new `LocalScript`
4. Copy and paste the complete script
5. Save and test!

### Server Script (Optional - for checkpoint reset)
Required only if you want the checkpoint reset functionality to work properly.

Place in `ServerScriptService`:

```lua
--[[
    Basecamp Reset System - Server Script
    Compatible with: StatsCore Sequential CP System
]]

local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

-- Create or get RemoteEvent
local resetEvent = ReplicatedStorage:FindFirstChild("ResetCheckpointEvent")
if not resetEvent then
    resetEvent = Instance.new("RemoteEvent")
    resetEvent.Name = "ResetCheckpointEvent"
    resetEvent.Parent = ReplicatedStorage
end

-- Handle checkpoint reset
resetEvent.OnServerEvent:Connect(function(player, action)
    if action == "ResetCheckpoint" then
        -- Reset checkpoint logic
        local leaderstats = player:FindFirstChild("leaderstats")
        if leaderstats then
            local stage = leaderstats:FindFirstChild("Stage")
            if stage then
                stage.Value = 0 -- Reset to stage 0
                print("✓ Checkpoint reset for " .. player.Name)
            end
        end
    end
end)

print("✓ Basecamp Reset System Loaded (SERVER)")
```

## 🎮 Usage

### Opening the Menu
- Click the **hamburger menu button** (top-right corner)
- Menu opens with smooth animation

### Using Features
1. Click on any category to expand it
2. Toggle switches to enable/disable features
3. Features activate instantly
4. Click **Reset to Base** for instant teleport (menu closes automatically)

### Closing the Menu
- Click the **X button** or **hamburger menu** again
- Menu closes instantly (no animation for fast response)

## 🎨 UI Features

- **Responsive Design** - Automatically adapts to PC and Mobile
- **Modern Aesthetics** - Discord-inspired color scheme
- **Smooth Animations** - Opening animations with instant closing
- **Category System** - Organized features in expandable categories
- **Visual Feedback** - Hover effects and status indicators
- **Breathing Effect** - Subtle glow animation on toggle button

## ⚙️ Configuration

### Basecamp Detection
The script automatically searches for these object names:
- `Basecamp`
- `SpawnLocation`
- `Base`
- `Spawn`

If none found, defaults to position: `Vector3.new(0, 50, 0)`

### Customization
You can modify colors in the `COLORS` table:
```lua
local COLORS = {
    primary = Color3.fromRGB(88, 101, 242),
    secondary = Color3.fromRGB(114, 137, 218),
    background = Color3.fromRGB(25, 28, 33),
    -- ... more colors
}
```

## 📱 Platform Support

### PC
- Full keyboard and mouse support
- Hover effects
- Optimized button sizes

### Mobile
- Touch-optimized controls
- Adjusted UI scaling
- Smaller button sizes for better mobile UX

## 🔧 Technical Details

- **No LocalStorage/SessionStorage** - Uses in-memory state management
- **Persistent GUI** - `ResetOnSpawn = false`
- **High DisplayOrder** - GUI appears above other elements
- **Safe Connections** - Protected event connections with error handling
- **Cleanup System** - Automatic cleanup on script removal

## 📝 Changelog

### v2.2.0 (Current)
- ✨ Added Reset to Base feature with server sync
- ⚡ Instant menu closing (no animation)
- 🔄 Renamed Teleport category to Reset
- 🐛 Bug fixes and improvements

### v2.1.2
- ✨ Hide All UI now preserves PlayerList, Chat, and Emotes Menu
- 🎥 Spectator Mode improvements

### v2.0.0
- 🎨 Complete UI redesign
- 📱 Mobile support
- 🗂️ Category system implementation

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

**ItoRenz00**

## 🙏 Credits

- Inspired by modern Discord UI design
- Built for the ROBLOX community

## ⚠️ Disclaimer

This script is provided "as is" without warranty of any kind. Use at your own risk. Always test in a private server before using in production games.

## 🐛 Known Issues

- None reported yet

## 📞 Support

If you encounter any issues or have suggestions:
1. Open an issue on GitHub
2. Provide detailed information about the problem
3. Include your ROBLOX Studio version

---

**⭐ If you find this useful, please give it a star!**
