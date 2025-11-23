<div align="center">

<img src="https://i.imgur.com/89n3apz.jpeg" alt="LSurvival Teleport Logo" width="100%"/>

# 🌀 LSurvival Teleport
### The Ultimate "Lag-Free" Teleportation System for RocketMod 4

![RocketMod](https://img.shields.io/badge/RocketMod-4-blue?style=flat-square&logo=csharp)
![Unturned](https://img.shields.io/badge/Game-Unturned-green?style=flat-square&logo=steam)
![Performance](https://img.shields.io/badge/Performance-Zero_Lag-blueviolet?style=flat-square)
![Status](https://img.shields.io/badge/Status-Production_Ready-success?style=flat-square)

<p align="center">
  <b>LSurvival Teleport</b> is a professional-grade TPA plugin engineered for high-population servers.
  <br>
  It abandons legacy "polling loops" in favor of <b>Unity Coroutines</b> and <b>Event-Driven Logic</b>, ensuring zero impact on server FPS even with hundreds of active players.
</p>

---

</div>

## 📑 Table of Contents
- [Why Choose This Plugin?](#-why-choose-this-plugin)
- [Key Features](#-key-features)
- [Visual Experience](#-visual-experience)
- [Commands](#-commands)
- [Configuration](#-configuration)
- [Acknowledgments](#-acknowledgments)

---

## 🚀 Why Choose This Plugin?



* **Zero Idle Usage:** When no one is teleporting, the plugin consumes **0% CPU**.
* **Unity Coroutines:** Teleport delays (e.g., "Wait 3 seconds") are handled natively by the engine's coroutine system, not by heavy loop checks.
* **Fair Play Design:** No "Pay-to-Win" cooldowns. A unified, balanced experience for all players.

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **🛡️ Anti-Combat** | Integrated `CombatManager` automatically blocks TPA requests if players are in PvP. |
| **🚫 Vehicle Glitch Protection** | Prevents players from accepting requests while inside vehicles, stopping map exploits and flying cars. |
| **📉 Anti-Lag Architecture** | Built with `UniTask` principles and thread-safe dispatchers. Safe for high-pop servers. |
| **🎨 Dynamic Icons** | Context-aware UI Icons (Success, Error, Combat, Warning) included in every message. |
| **🌍 Multi-Language** | Native support for **English (EN)**, **Spanish (ES)**, and **Portuguese (PT)**. |

---

## 🎨 Visual Experience

This plugin delivers a Premium UI experience out of the box. It features **Hardcoded High-Quality Icons** that cannot be tampered with, ensuring a consistent server aesthetic:

* ✅ **Success:** Green Check icon for completed actions.
* ❌ **Error:** Red Cross icon for denied/failed requests.
* ⚔️ **Combat:** Sword/Shield icon when blocked by PvP.
* ⚠️ **Warning:** Yellow Alert icon for cooldowns.

---

## ⌨️ Commands

The plugin uses a unified command structure to keep the chat clean.

| Command | Syntax | Description |
| :--- | :--- | :--- |
| **Send Request** | `/tpa <player>` | Sends a teleport request to a player. |
| **Accept** | `/tpa a` | Accepts the pending request. |
| **Deny** | `/tpa d` | Denies the pending request. |
| **Cancel** | `/tpa c` | Cancels a request you sent. |

> **Note:** If a player types `/tpa` without arguments, the plugin intelligently displays the help menu.

---

## ⚙️ Configuration

Optimized default settings for survival gameplay:

```xml
<LSurvivalTeleportConfiguration>
  <Language>ES, EN, PT </Language> <RequestDurationSeconds>15</RequestDurationSeconds>
  <TeleportDelaySeconds>3</TeleportDelaySeconds>
  <CooldownSeconds>60</CooldownSeconds>
  
  <BlockInCombat>true</BlockInCombat>
  <CombatCooldownSeconds>20</CombatCooldownSeconds>
  <CancelOnMove>true</CancelOnMove>
</LSurvivalTeleportConfiguration>
