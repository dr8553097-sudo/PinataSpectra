# 🪅 PinataSpectra Sovereign Edition — Official Documentation

<div align="center">
  <span class="badge-premium">★ SOVEREIGN COMMERCIAL EDITION ★</span>
</div>

> [!IMPORTANT]
> **This documentation is strictly for PinataSpectra — Sovereign Edition (Commercial / Premium Release).**
> 
> * **PinataSpectra Lite (Free Version):** A basic demonstration version with limited single-phase mechanics is maintained in a separate repository with its own dedicated lightweight documentation. The Lite edition does NOT include multi-tier combat phases, particle LOD, ephemeral candy sweeps, auto-schedulers, or 54-slot async GUI leaderboards.
> * **Sovereign Edition (This Plugin):** Contains the complete enterprise suite designed for large communities (80+ concurrent players) with zero tick overhead.

---

## 🌟 Sovereign Edition vs Lite vs Generic Pinata Plugins

| Feature / Architecture | 🪅 PinataSpectra Sovereign (This Version) | 🍃 PinataSpectra Lite (Free) | 📦 Generic / Legacy Pinata Plugins |
|---|:---:|:---:|:---:|
| **Entity Technology** | Native `ItemDisplay` & `Interaction` | Native `ItemDisplay` | Obsolete Invisible ArmorStands (High Packets) |
| **80+ Players Concurrent Performance** | **20.0 TPS Stable** (Particle LOD) | 20.0 TPS (Basic) | Client FPS Drops & Server Stutters |
| **Physics Engine** | 3D Catenary Rope & Harmonic Recoil | Static Floating | Static or Basic ArmorStand Leash |
| **Combat Mechanics** | **4 Dynamic Phases** (Shields & Minions) | Single Health Bar | Single Health Bar |
| **Emotion Morphing** | 4 Dynamic Facial State Morphs | Static Texture | None |
| **Arena Runes** | Animated Ground Runic Perimeter Circle | None | None |
| **Combat Candies** | Ephemeral Candies + **Auto-Sweeper Purge** | None | Permanent Candies (Dupe/Economy Risk) |
| **Leaderboard System** | **54-Slot Async GUI** + Multi-Category DB | Chat Text Only | None or Basic Flatfile |
| **Automation** | **Auto-Scheduler Engine** with Alerts | None | Manual Commands Only |
| **Vote Goal / BossBar** | Community BossBar + NuVotifier Goal | None | None |
| **Custom Model Engine / Oraxen** | Native Hook Support | None | None |
| **Database Storage** | SQLite / MySQL / Redis Pool (HikariCP) | Local Flatfile | YAML Flatfile Only |

---

## 🧭 Documentation Index

Explore the modules in sequence:

1. 🏛️ [**01. Architecture & Performance**](01-Architecture-and-Performance.md) — Asynchronous database engine, thread-safety, and 20.0 TPS guarantees.
2. ⚙️ [**02. Installation & Setup**](02-Installation-and-Setup.md) — Paper/Purpur 1.20 - 1.26+ requirements, Java 21/25, and optional hooks.
3. 🦄 [**03. 3D Display Entities & Physics**](03-3D-Display-Entities-and-Physics.md) — Real-time suspension, angular impulse, and facial emotion morphing.
4. ⚔️ [**04. Combat Phases & Boss Mechanics**](04-Combat-Phases-and-Boss-Mechanics.md) — Deep dive into the 4-phase combat state machine.
5. 🛠️ [**05. Creating Custom Piñatas**](05-Creating-Custom-Pinatas.md) — **Complete step-by-step tutorial** on crafting custom piñatas from scratch.
6. 🔮 [**06. Particle LOD & Runic Circles**](06-Particle-LOD-and-Runic-Circles.md) — Multi-tier distance optimization and animated floor perimeters.
7. 🍬 [**07. Ephemeral Candies & Sweeper**](07-Ephemeral-Candies-and-Sweeper.md) — Active event consumption rules and automatic economy purges.
8. 🏆 [**08. Leaderboards GUI & Stats**](08-Leaderboards-GUI-and-Stats.md) — 54-slot interactive menu (`/pinata top`) with SQLite/MySQL.
9. ⏳ [**09. Auto-Scheduler & Vote Party**](09-Auto-Scheduler-and-Vote-Party.md) — Timed recurring spawns and community vote goal BossBar.
10. 📜 [**10. Master Configuration Reference**](10-Master-Configuration-Reference.md) — Exhaustive line-by-line configuration guide.
11. 🧩 [**11. Commands & Placeholders**](11-Commands-Permissions-and-Placeholders.md) — Complete command, permission, and PlaceholderAPI reference.
12. 💻 [**12. Developer API & Best Practices**](12-Developer-API-and-Events.md) — Java API, Bukkit events, and enterprise security warnings.
13. ⚖️ [**13. Detailed Edition Comparison**](13-Comparison-and-Editions.md) — Full comparison matrix and feature breakdown.

---

<div align="right">

[**01. Architecture & Performance →**](01-Architecture-and-Performance.md)

</div>
