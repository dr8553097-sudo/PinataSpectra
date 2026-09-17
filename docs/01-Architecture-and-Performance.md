# 🏛️ 01. Architecture & Enterprise Performance

**PinataSpectra — Sovereign Edition** is engineered specifically for high-concurrency Minecraft networks. Traditional event plugins frequently suffer from TPS drops, packet floods, and client-side FPS lag when dozens of players congregate in a single arena. PinataSpectra eliminates these bottlenecks through modern entity architectures and multi-threaded processing.

---

## ⚡ 1. Modern Display Entities vs. Legacy ArmorStands

| Aspect | PinataSpectra (Display Entities) | Legacy Plugins (ArmorStands) |
|---|---|---|
| **Entity Type** | Native `ItemDisplay` & `Interaction` (1.20+) | 10-30 Invisible `ArmorStand` entities |
| **Packet Overhead** | Minimal (Single entity transformation packet) | Heavy (Continuous equipment & movement sync packets) |
| **Hitbox Accuracy** | Pixel-perfect customized `Interaction` bounding box | Clunky ArmorStand bounding boxes |
| **Client FPS Impact** | **0 FPS drop** (interpolated on GPU) | Severe FPS drops on low-end client PCs |

---

## 🧵 2. Asynchronous Multi-Threaded Data Flow

```
[Main Server Thread (Paper/Purpur)]
  │ ──> Handles Player Hits & Combat Event Verification
  │ ──> Dispatches State Transitions & Animation Transforms
  ▼
[Async Worker Threads (ForkJoinPool / HikariCP)]
  ├── Database Sync (SQLite / MySQL updates for Top Damage, MVP, Candies)
  ├── Leaderboard Sorting & Query Caching
  ├── Webhook Notifications (Discord Embeds)
  └── Candy Sweeper Inventory Audits
```

* **Zero Main-Thread Blocking:** Database transactions, ranking queries, and inventory sweeps are strictly executed on background worker threads.
* **Connection Pooling:** Built-in **HikariCP** pool guarantees microsecond database operations with automatic reconnects.

---

<div align="space-between">

[**← Home / Overview**](Home.md) | [**02. Installation & Setup →**](02-Installation-and-Setup.md)

</div>
