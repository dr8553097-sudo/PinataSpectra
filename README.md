<p align="center">
  <img src="assets/banner.png" alt="PinataSpectra Banner" width="100%" style="max-width: 850px;">
</p>
<p align="center">
  <a href="https://github.com/dr8553097-sudo/PinataSpectra"><img src="https://img.shields.io/badge/Version-1.0.0--RELEASE-purple.svg?style=for-the-badge" alt="Version"></a>
  <a href="https://papermc.io"><img src="https://img.shields.io/badge/Paper%20%2F%20Purpur-1.20%20--%201.26+-00f0ff.svg?style=for-the-badge" alt="Platform"></a>
  <a href="https://www.java.com"><img src="https://img.shields.io/badge/Java-21%20%2F%2025-orange.svg?style=for-the-badge" alt="Java"></a>
  <a href="https://github.com/dr8553097-sudo/PinataSpectra/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-Commercial%20EULA-red.svg?style=for-the-badge" alt="License"></a>
  <a href="https://dr8553097-sudo.github.io"><img src="https://img.shields.io/badge/Portfolio-Dafealru-a855f7.svg?style=for-the-badge" alt="Portfolio"></a>
</p>

---

## 🌟 Overview / Visión General

**PinataSpectra** is an enterprise-grade Minecraft plugin engineered for **Paper, Purpur, and Spigot (1.20 - 1.26+)**. It elevates community server events with procedural 3D Display Entity piñatas, reactive 4-phase combat mechanics, intelligent particle Level of Detail (LOD), dynamic ground runic circles, ephemeral combat candies, vote parties, and a 54-slot async GUI leaderboard.

> **Zero Tick Overhead:** All database tracking, leaderboard queries, hologram math, and event sweeps are processed off the main server thread to guarantee a solid **20.0 TPS** even during 80+ player boss fights.

---

## 🎬 Gameplay & Showcase Clips / Demostraciones en Video

| Preview | Video File | Description |
|---|---|---|
| 🎮 **Gameplay Combat** | [`assets/clip_1_gameplay.mp4`](assets/clip_1_gameplay.mp4) | In-game combat, physics, hitboxes & particle effects |
| 🛡️ **Shield & Phases** | [`assets/clip_2_features.mp4`](assets/clip_2_features.mp4) | 4-phase transitions, minion spawns, runic circles & candy consumption |
| 🏆 **Event Finale & GUI** | [`assets/clip_3_showcase.mp4`](assets/clip_3_showcase.mp4) | Grand loot explosion, 54-slot Leaderboard GUI & candy sweep |

---

## ⚡ Key Features / Características Principales

### 🦄 1. Procedural 3D Display Entity Engine
- Utilizes native `ItemDisplay` and `Interaction` entities with zero dependency on client mods.
- Realistic rope suspension physics with harmonic swaying, recoil impulse upon hits, and continuous floating rotation.
- **Emotion Morphing:** Dynamic face texture changes transitioning across *Calm*, *Nervous*, *Angry (Enraged)*, and *Dying*.

### ⚔️ 2. Dynamic 4-Phase Combat State Machine (`PinataPhaseStateMachine`)
- **Phase 1 (Calm):** Initial damage phase with reactive dialogue quotes.
- **Phase 2 (Shield / Minions):** Spawns a magical defensive shield absorbing hits until guardian minions are defeated.
- **Phase 3 (Rage / Frenzy):** Knockback pulses, lightning strikes, and enraged particle auras.
- **Phase 4 (Final Stand / Chaos Drop):** High-speed floating and epic progressive loot explosion.

### 🔮 3. Smart Particle LOD & Runic Ground Circles
- **Level of Detail (LOD):** Automatically adjusts particle frequency and render distance based on nearby player density to prevent FPS drops on low-end client machines.
- **Runic Floor Circles:** Animated rotating circular particle runes project directly onto the ground beneath floating piñatas.

### 🍬 4. Ephemeral Candies & Candy Sweeper Engine
- Special consumable candies (Buffs, Speed, Regeneration, Strength) that can **only be used while a Piñata event is active**.
- **Global Sweeper Service:** Automatically purges remaining event candies from player inventories, enderchests, and world drops as soon as the event concludes to protect the server economy.

### 🏆 5. 54-Slot Async GUI Leaderboard (`/pinata top`)
- Live ranking GUI with animated glass borders, persistent SQLite/MySQL tracking for:
  - 💥 **Top Damage Dealers**
  - 👑 **Top Piñata MVPs (Last Hit / Slayers)**
  - 🍬 **Top Candies Consumed**

### ⏳ 6. Automated Event Scheduler & Vote Party / Donation Goal
- Set automated recurring piñata spawns by interval with advance countdown announcements.
- **Community Vote Goal:** Accumulates server votes (`/pinata vote add`) with a dynamic community BossBar triggering a Piñata Party once the goal is reached.

---

## 📜 Commands & Permissions

| Command | Permission | Description |
|---|---|---|
| `/pinata spawn <type> [tier]` | `pinataspectra.admin` | Spawns a 3D Piñata at your target location |
| `/pinata top` | `pinataspectra.player` | Opens the 54-slot Interactive Top Leaderboard GUI |
| `/pinata killall` | `pinataspectra.admin` | Instantly removes all active Piñatas and cleans entities |
| `/pinata vote [add\|set] <amount>` | `pinataspectra.admin` | Adds or sets votes towards the Community Vote Party Goal |
| `/pinata scheduler [toggle\|next]` | `pinataspectra.admin` | Manages the automated timed scheduler engine |
| `/pinata sweepcandies` | `pinataspectra.admin` | Manually triggers the global Candy Sweeper purge |
| `/pinata reload` | `pinataspectra.admin` | Hot-reloads all configuration and message files |

---

## 🧩 PlaceholderAPI Support

| Placeholder | Description |
|---|---|
| `%pinataspectra_active_count%` | Number of currently active Piñatas in all worlds |
| `%pinataspectra_vote_current%` | Current votes accumulated towards the next Vote Party |
| `%pinataspectra_vote_required%` | Target votes required to trigger a Vote Party |
| `%pinataspectra_vote_percent%` | Progress percentage of the Vote Party goal |
| `%pinataspectra_scheduler_time%` | Formatted countdown until the next scheduled Piñata |
| `%pinataspectra_top_damage_1_name%` | Player name with highest total damage dealt |
| `%pinataspectra_top_damage_1_value%`| Total damage points of #1 damage dealer |
| `%pinataspectra_top_broken_1_name%` | Player name with most Piñatas destroyed (MVP) |
| `%pinataspectra_top_candies_1_name%`| Player name with most event candies consumed |

---

## 🛠️ Installation

1. Download `PinataSpectra-1.0.0-RELEASE.jar`.
2. Place the JAR file in your server's `/plugins/` folder.
3. *(Optional)* Install [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) and [DecentHolograms](https://www.spigotmc.org/resources/decentholograms.96927/).
4. Start or restart your server.
5. Customize `config.yml`, `pinatas.yml`, and `messages.yml` to your liking.

---

## 💻 Developer API

```java
import net.dafealru.pinataspectra.PinataSpectra;
import net.dafealru.pinataspectra.pinata.PinataInstance;

// Access active pinata instances
PinataSpectra plugin = PinataSpectra.getInstance();
for (PinataInstance pinata : plugin.getPinataManager().getActivePinatas().values()) {
    double healthPercent = pinata.getHealthPercent();
    int currentPhase = pinata.getStateMachine().getCurrentPhase();
    // Custom server integration logic
}
```

---

## 👤 Author & Support

- **Developer:** [Dafealru (dr8553097-sudo)](https://dr8553097-sudo.github.io)
- **Portfolio:** [https://dr8553097-sudo.github.io](https://dr8553097-sudo.github.io)
- **GitHub:** [https://github.com/dr8553097-sudo](https://github.com/dr8553097-sudo)

Developed with ❤️ for high-performance Minecraft server communities.

