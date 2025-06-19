# MIA Admin Control Panel v2.0.0

🛡️ **Advanced Admin Control Panel for ESX Legacy FiveM Servers**

A comprehensive, modern admin panel with real-time management capabilities, multi-database compatibility, and an intuitive in-game NUI interface.

## 📋 Features

### 🎮 **Complete Server Management**
- **Real-time Player Monitoring** - Live player statistics and management
- **Resource Control** - Start, stop, and restart server resources
- **Economy Management** - Full control over player money and items
- **Vehicle System** - Spawn vehicles directly from your database
- **Advanced Job System** - Create and manage jobs with multi-level grades
- **Weapons Arsenal** - Complete weapon distribution and loadout management
- **Player Analytics** - Comprehensive logging and activity tracking

### 🎨 **Modern Design**
- Clean, professional dark theme interface
- Responsive floating panel design (1200x800px)
- Smooth animations and transitions
- Mobile-friendly responsive layout
- No gameplay obstruction

### 🔒 **Security & Permissions**
- Role-based permission system (superadmin, admin, moderator)
- Secure admin verification
- Comprehensive action logging
- Real-time notifications

## 📁 File Structure

```
mia_admincontrol/
├── fxmanifest.lua          # Resource manifest
├── config/
│   └── config.lua          # Main configuration file
├── server/
│   ├── main.lua           # Core server functions
│   ├── events.lua         # Player & resource management events
│   ├── weapons.lua        # Weapon management events
│   └── logging.lua        # Database & logging system
├── client/
│   └── main.lua           # Client-side functionality
├── html/
│   ├── index.html         # Main UI interface
│   ├── style.css          # Modern styling
│   └── script.js          # JavaScript functionality
└── README.md              # This documentation
```

## 🚀 Installation

1. **Download** the `mia_admincontrol` folder to your server's `resources` directory

2. **Add to server.cfg:**
   ```cfg
   ensure mia_admincontrol
   ```

3. **Database Setup:**
   - The resource automatically creates required tables (`player_logs`, `bans`)
   - Ensure your server has the `vehicles`, `jobs`, and `job_grades` tables

4. **Dependencies:**
   - ESX Legacy Framework
   - MySQL-Async

## ⚙️ Configuration

### Admin Permissions
Edit `config/config.lua` to customize admin groups and permissions:

```lua
Config.AdminGroups = {
    'superadmin',
    'admin', 
    'moderator'
}
```

### UI Settings
```lua
Config.UI = {
    keybind = 'F10',           -- Default keybind
    showNotifications = true,   -- Enable notifications
    autoRefresh = true,        -- Auto refresh data
    theme = 'dark'             -- UI theme
}
```

### Weapon Loadouts
Customize pre-defined weapon loadouts:
```lua
Config.Loadouts = {
    ['police'] = {
        {weapon = 'WEAPON_COMBATPISTOL', ammo = 250},
        {weapon = 'WEAPON_STUNGUN', ammo = 1}
    }
}
```

## 🎯 Usage

### Opening the Panel
- **Command:** `/admin` (configurable)
- **Keybind:** F10 (configurable)
- **Permission:** Requires admin, superadmin, or moderator group

### Navigation
- **Dashboard** - Server overview and statistics
- **Players** - Player management and actions
- **Resources** - Control server resources
- **Vehicles** - Vehicle spawning from database
- **Economy** - Money and item management
- **Player Logs** - Analytics and activity tracking
- **Job Management** - Create and manage server jobs
- **Weapons** - Advanced weapon distribution

### Key Functions

#### Player Management
- Kick/ban players with reasons
- Teleport to/from players
- View player statistics
- Real-time player monitoring

#### Economy Control
- Give cash, bank money, or dirty money
- Distribute items to players
- Track all economic transactions

#### Vehicle System
- Spawn any vehicle from your database
- Organized by categories and pricing
- Support for custom addon vehicles

#### Job Management
- Create new jobs with whitelisting options
- Multi-level grade system with salaries
- Assign players to jobs instantly

#### Weapons Arsenal
- 40+ weapon types available
- Pre-configured loadouts (Police, SWAT, Military, etc.)
- Individual weapon distribution
- Real-time weapon tracking

## 🔧 Customization

### Adding Custom Items
Edit the items list in `config/config.lua`:
```lua
Config.Items = {
    {name = 'custom_item', label = 'Custom Item'}
}
```

### Custom Weapon Loadouts
Add new loadouts to the configuration:
```lua
Config.Loadouts = {
    ['custom_loadout'] = {
        {weapon = 'WEAPON_PISTOL', ammo = 100}
    }
}
```

### Permission Levels
Customize which admin groups can perform specific actions:
```lua
Config.Permissions = {
    ['kick'] = {'superadmin', 'admin', 'moderator'}
}
```

## 📊 Database Tables

The resource automatically creates and manages:

### player_logs
- Tracks all player activities and admin actions
- Includes timestamps, player info, and action details
- Used for analytics and audit trails

### bans (if not exists)
- Stores player ban information
- Includes expiration dates and ban reasons
- Integrates with ESX ban system

## 🛠️ Troubleshooting

### Common Issues

**Panel won't open:**
- Check admin permissions in database
- Verify ESX is loaded properly
- Check console for errors

**Database errors:**
- Ensure MySQL-Async is installed
- Check database connection
- Verify table permissions

**Vehicle spawning issues:**
- Check `vehicles` table exists
- Verify vehicle models are valid
- Check spawn permissions

### Console Commands
```
/admin - Opens admin panel (with permissions)
```

## 📝 Changelog

### v2.0.0
- Complete resource reorganization
- Modular file structure
- Enhanced permission system
- Advanced logging capabilities
- Improved UI/UX design
- Added weapons management
- Enhanced job system
- Better error handling

## 🤝 Support

For support and updates:
- Report issues with detailed error logs
- Include server setup information
- Provide steps to reproduce problems

Copyright (c) [MiaGamingDev] [2025]

This script and its associated files are the intellectual property of the author and are protected under copyright law.

By purchasing, downloading, or using this script (hereafter referred to as “the Product”), you agree to the following terms:

1. LICENSE GRANT
   - You are granted a **non-exclusive**, **non-transferable**, and **revocable** license to use this script on **one (1) server only**, unless otherwise specified.

2. RESTRICTIONS
   - You may NOT resell, redistribute, share, leak, or modify this script for resale.
   - You may NOT use any part of this script in other public or paid resources without explicit written permission.
   - You may NOT deobfuscate, decrypt, or bypass protections (e.g., escrow or licensing).

3. OWNERSHIP
   - This script remains the full intellectual property of the original author.
   - Purchasing this script does **not** transfer ownership.

4. SUPPORT & UPDATES
   - Support is provided only to verified customers.
   - Updates are not guaranteed, but may be provided at the author's discretion.

5. VIOLATION
   - Any violation of this license may result in a permanent ban from future access, and potential legal action.

If you do not agree with these terms, you are not authorized to use this script.

 This resource is "protected by Cfx.re escrow system".

Signed,
[MiaGamingDev]

**MIA Admin Control Panel** - Professional server management made simple.
