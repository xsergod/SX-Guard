# 🛡️ SXGuard Anti-Cheat System

[![Minecraft Versions](https://img.shields.io/badge/Minecraft-1.12%20to%2021-blue.svg)](https://www.minecraft.net)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-0.1--demo-orange.svg)](https://github.com/xsergod/SX-Guard/releases)
[![Discord](https://img.shields.io/discord/1206332178875818014?logo=discord)](https://discord.gg/yBZXkaJj4J)
[![Code Style](https://img.shields.io/badge/code%20style-google%20java-ff69b4.svg)](https://google.github.io/styleguide/javaguide.html)

## 📖 Overview

**SXGuard** is a next-generation, modular anti-cheat system for Minecraft servers (versions 1.12 to 1.21). Built with performance, accuracy, and extensibility in mind, it provides comprehensive protection against a wide range of cheats while minimizing false positives.

## ✨ Key Features

### 🔍 **Advanced Detection Methods**
- **Multi-Layer Detection**: Combines rule-based, pattern-based, and statistical analysis
- **Behavioral Analysis**: Learns and adapts to individual player patterns
- **Physics Validation**: Ensures all actions comply with Minecraft physics
- **Real-time Prediction**: Predicts and validates player movements

### ⚡ **Performance Optimized**
- Intelligent cooldown management
- Early-exit checks for exemptions
- Caching frequently accessed data
- Batch processing for multiple checks
- TPS-aware confidence scoring

### 🛡️ **Checks**
**Combat** :
- AimBot
- AntiKB
- AutoClicker
- CPSPattern
- Criticals
- FastBow
- HitBox
- KillAura
- LegitSwingCheck
- MultiAura
- PerfectTracking
- Reach
- Smooth Aim Pattern
- TriggerBot
- VelocityModification

**Movement** :
- AirStrafe
- BHop
- FastLadder
- FastSneak
- Fly
- Glide
- HighJump
- Jesus
- NoFall
- NoSlow
- Phase
- Speed
- Spider
- Step
- Timer

**Player** :
- AutoTotem
- AutoArmor
- Blink
- FastPlace
- FastUse
- InventoryMove
- Nuker
- Scaffold
- Tower
- XCarry

**World** :
- BadPackets
- FakeRotation
- FastBreak
- GhostHand
- IllegalInteract
- InvalidMovement
- NoInventoryCooldown
- PacketFly
- PacketMine
- ServerCrasherMovementLoop

## 🚀 Quick Start

### Prerequisites
- Java 1.8 or higher
- Spigot/Paper 1.12-1.21
- 2GB+ RAM recommended

### Installation
1. Download the latest release from [Releases](https://github.com/xsergod/SX-Guard/releases)
2. Place `SXGuard.jar` plugin in your `plugins/` folder
3. Download [Protocolib Plugin](https://www.spigotmc.org/resources/protocollib.1997/) and Place Plugin in your `plugins/` folder
3. Restart your server
4. Configure settings in `plugins/SXGuard/config.yml`

### Basic Configuration
```yaml
# plugins/SXGuard/config.yml
#punishment Types : (kick, ban, warn, alert)
# Warn type for send warning to player
Speed:
  enabled: true
  threshold: 15.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

Fly:
  enabled: true
  threshold: 8.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 1440

Glide:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

NoFall:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Spider:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

Step:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

HighJump:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Jesus:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

AirStrafe:
  enabled: true
  threshold: 15.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

BHop:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Timer:
  enabled: true
  threshold: 15.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 720

FastLadder:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

Phase:
  enabled: true
  threshold: 5.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 2880

NoSlow:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

FastSneak:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

KillAura:
  enabled: true
  threshold: 12.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 4320

TriggerBot:
  enabled: true
  threshold: 15.0
  violation-amount: 1.5
  punishment: "ban"
  duration: 2160

Aimbot:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Reach:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

AutoClicker:
  enabled: true
  threshold: 10.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

MultiAura:
  enabled: true
  threshold: 8.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 1440

VelocityModification:
  enabled: true
  threshold: 12.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

AntiKB:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Criticals:
  enabled: true
  threshold: 15.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

HitBox:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

LegitSwingCheck:
  enabled: true
  threshold: 10.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

PerfectTracking:
  enabled: true
  threshold: 12.0
  violation-amount: 1.5
  punishment: "ban"
  duration: 1440

FastBow:
  enabled: true
  threshold: 10.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

SmoothAimPattern:
  enabled: true
  threshold: 15.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

CPSPattern:
  enabled: true
  threshold: 10.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

InventoryMove:
  enabled: true
  threshold: 15.0
  violation-amount: 1.0
  punishment: "kick"
  duration: 0

AutoArmor:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

FastUse:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

AutoTotem:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Scaffold:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

Tower:
  enabled: true
  threshold: 10.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

Nuker:
  enabled: true
  threshold: 8.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 1440

FastPlace:
  enabled: true
  threshold: 12.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

XCarry:
  enabled: true
  threshold: 5.0
  violation-amount: 2.0
  punishment: "kick"
  duration: 0

Blink:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

PacketFly:
  enabled: true
  threshold: 5.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 4320

InvalidMovement:
  enabled: true
  threshold: 3.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 10080

BadPackets:
  enabled: true
  threshold: 5.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 2880

FastBreak:
  enabled: true
  threshold: 10.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

PacketMine:
  enabled: true
  threshold: 8.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 1440

GhostHand:
  enabled: true
  threshold: 5.0
  violation-amount: 2.0
  punishment: "kick"
  duration: 0

IllegalInteract:
  enabled: true
  threshold: 3.0
  violation-amount: 2.0
  punishment: "ban"
  duration: 10080

NoInventoryCooldown:
  enabled: true
  threshold: 10.0
  violation-amount: 1.2
  punishment: "kick"
  duration: 0

FakeRotation:
  enabled: true
  threshold: 8.0
  violation-amount: 1.5
  punishment: "kick"
  duration: 0

ServerCrasherMovementLoop:
  enabled: true
  threshold: 3.0
  violation-amount: 3.0
  punishment: "ban"
  duration: 10080
```

### Customizing Messages
```yaml
# plugins/SXGuard/messages.yml
prefix: "&8[&cSX_Guard&8]"

no-permission: "&cYou don't have permission to use this command."
player-only-command: "&cThis command can only be used by players."
player-not-found: "&cPlayer not found!"

reload-success: "&aConfiguration reloaded successfully!"
reload-failed: "&cConfiguration reload failed!"

alerts-enabled: "&aAlerts enabled!"
alerts-disabled: "&cAlerts disabled!"
alerts-format: "&8[&cSX_Guard&8] &7%player% &ffailed &c%check% &7(VL: %vl%)"

kick-message: "&cUnfair advantage detected! (%check%)"
ban-message: "&cCheating detected! Banned for %duration% minutes. (%check%)"
warning-message: "&cPlease stop using unfair advantages! (%check%)"

punishments:
  kick:
    message: |
      &8&m-----------------------------------------------------
      &c&lSX_Guard Anti-Cheat System
      &8&m-----------------------------------------------------
      &7You were kicked for suspicious activity
      &7Detection: &f%check%
      &7Violation Level: &f%vl%
      &7Time: &f%time%
      
      &eIf this is a mistake, please contact staff.
      &8&m-----------------------------------------------------

  ban:
    screen-message: |
      &8&m-----------------------------------------------------
      &4&lSX_Guard Anti-Cheat System
      &8&m-----------------------------------------------------
      &cYour account has been banned
      &7Reason: &f%description%
      &7Detection: &f%check%
      &7Violation Level: &f%vl%
      &7Duration: &f%duration%
      &7Time: &f%time%
      
      &eYou can appeal at our discord server.
      &8&m-----------------------------------------------------
    banlist-reason: "SX_Guard | %check% (VL: %vl%)"

  alert:
    message: "&8[&c⚠&8] &cSX_Guard &8» &7Unfair play detected: &f%check% &8(&7VL: &f%vl%&8) &cPlease stop!"

  duration:
    permanent: "Permanent"
    minutes: "minute"
    hours: "hour"
    days: "day"

notifications:
  staff-broadcast: "&8[&6⚡&8] &eSX_Guard &8» &c%player% &7was &f%type% &7for &f%check% &8(&7VL: &f%vl%&8)"
  staff-broadcast-enabled: true
  join-notification: "&aSX_Guard is actively monitoring for cheats."
  update-available: "&aA new update for SX_Guard is available!"

alerts:
  title:
    main: "§c§lWARNING"
    subtitle: "§7Unfair play detected"
  action-bar: "§c⚠ %check% detected! VL: %vl%"

status-format:
  header: "&8=== &cSX_Guard Status &8==="
  player: "&7Player: &f%player%"
  ping: "&7Ping: &f%ping%ms"
  tps: "&7TPS: &f%tps%"
  alerts: "&7Alerts: &f%alerts_status%"
  world: "&7World: &f%world%"
  location: "&7Location: &f%location%"
  violations-header: "&7Violations:"
  violation-format: "&8- &f%check%: &c%vl%"
  no-violations: "&7No violations"
  punishment-history: "&7Punishment History:"
  punishment-format: "&8- &f%type% &8(&7%check%&8) &7- &f%time%"
  no-punishments: "&7No recent punishments"

help-format:
  header: "&8=== &cSX_Guard Commands &8==="
  reload: "&c/sxguard reload &7- Reload configuration"
  status: "&c/sxguard status <player> &7- Check player status"
  alerts: "&c/alerts &7- Toggle anti-cheat alerts"
  punishments: "&c/sxguard punishments <player> &7- View punishment history"

debug-enabled: "&7Debug mode enabled"
debug-disabled: "&7Debug mode disabled"

vl-threshold-notification: "&cWarning: %player% has reached VL %vl% for %check%"

prevention:
  knockback-enforced: "&cAnti-KB prevention activated!"
  movement-corrected: "&7Movement corrected by anti-cheat"
  reach-limited: "&7Reach distance limited"

exemptions:
  player-exempted: "&aPlayer %player% is now exempt from checks"
  player-unexempted: "&cPlayer %player% is no longer exempt from checks"
  exemption-list: "&7Exempted players: &f%players%"
  no-exemptions: "&7No players are currently exempt"

bypass:
  enabled: "&aBypass mode enabled"
  disabled: "&cBypass mode disabled"

checks:
  reach:
    detection-message: "&cUnnatural reach distance detected"
    prevention-message: "&7Reach limited to normal distance"

  aimbot:
    detection-message: "&cSuspicious aiming patterns detected"
    prevention-message: "&7Aiming patterns corrected"

  antikb:
    detection-message: "&cKnockback modification detected"
    prevention-message: "&7Knockback enforced"

  speed:
    detection-message: "&cUnnatural movement speed detected"
    prevention-message: "&7Speed limited to normal values"

  fly:
    detection-message: "&cFlight detected without permission"
    prevention-message: "&7Flight prevented"

gui:
  main-title: "&8SX_Guard Control Panel"
  player-management-title: "&8Player Management - %player%"
  checks-title: "&8Checks Configuration"
  settings-title: "&8System Settings"

  buttons:
    player-management: "&bPlayer Management"
    checks-config: "&aChecks Configuration"
    system-settings: "&eSystem Settings"
    reload-config: "&6Reload Configuration"
    back: "&cBack"

  player-actions:
    view-status: "&aView Status"
    view-punishments: "&6Punishment History"
    toggle-exempt: "&eToggle Exemption"
    kick-player: "&cKick Player"

  check-states:
    enabled: "&aENABLED"
    disabled: "&cDISABLED"
    aggressive: "&6AGGRESSIVE"
    lenient: "&9LENIENT"

logging:
  punishment-log: "PUNISHMENT: %player% was %type%ed for %check% (VL: %vl%)"
  detection-log: "DETECTION: %player% failed %check% (VL: %vl%)"
  prevention-log: "PREVENTION: %player% was prevented from using %check%"
  exemption-log: "EXEMPTION: %player% was %action% from checks"

update:
  available: "&aA new update for SX_Guard is available! Version: %version%"
  download: "&eDownload: %url%"
  changelog: "&7Changelog: %changelog%"
  current-version: "&7Current version: %version%"
  latest-version: "&7Latest version: %version%"

placeholders:
  player: "%player%"
  check: "%check%"
  description: "%description%"
  vl: "%vl%"
  duration: "%duration%"
  time: "%time%"
  type: "%type%"
  world: "%world%"
  location: "%location%"
  ping: "%ping%"
  tps: "%tps%"
  alerts_status: "%alerts_status%"
  version: "%version%"
  url: "%url%"
  changelog: "%changelog%"
  players: "%players%"
  action: "%action%"
```


## 🌟 Support
- **Discord**: [Join our Discord](https://discord.gg/aCnvXsmCYG)


## 📊 Version Support

| Minecraft | Status | Notes |
|-----------|--------|-------|
| 1.21.x | ✅ Full Support | Latest features |
| 1.20.x | ✅ Full Support | Stable |
| 1.19.x | ✅ Full Support | Long-term support |
| 1.18.x | ✅ Full Support | Recommended |
| 1.17.x | ✅ Full Support | |
| 1.16.x | ✅ Full Support | |
| 1.15.x | ✅ Full Support | |
| 1.14.x | ✅ Full Support | |
| 1.13.x | ⚠️ Limited | Some features disabled |
| 1.12.x | ⚠️ Limited | Basic detection only |


---

## 🐛 Found a Bug?

**Did you find a bug or need support?** Join our Discord and open a ticket!

[![Discord](https://discordapp.com/api/guilds/1206332178875818014/widget.png?style=banner2)](https://discord.gg/Fhy3CSzbgG)


### Before Reporting:
1. Make sure you're using the Supported version
2. Have your logs ready (`logs/latest.log`)
3. Include steps to reproduce the bug

---

### Need Immediate Help?
- **Check our FAQ**: [Common Solutions](https://github.com/yourusername/sxguard/wiki/FAQ)
- **Search Issues**: [GitHub Issues](https://github.com/yourusername/sxguard/issues)
- **Community Help**: [Discord Community](https://discord.gg/YOUR_INVITE_CODE)

**Response Time**: We aim to respond to all tickets within 24 hours!

---

<div align="center">
  
[![Discord](https://img.shields.io/discord/1206332178875818014?color=7289DA&logo=discord&logoColor=white)](https://discord.gg/yBZXkaJj4J)
[![Support Server](https://img.shields.io/badge/Support-Live%20Chat-blue)](https://discord.gg/VFPeJK9aJZ)

</div>

---

**Disclaimer**: SXGuard is designed to assist server administrators in maintaining fair gameplay. No anti-cheat system is perfect, and occasional false positives may occur. Always verify before issuing permanent bans.
