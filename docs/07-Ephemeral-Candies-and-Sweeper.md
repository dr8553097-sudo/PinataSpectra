# 🍬 07. Ephemeral Candies & Economy Sweeper Service

**Ephemeral Candies** are tactical combat consumables that drop during active piñata encounters to empower players.

---

## 📜 Candy Rules & Mechanics

1. **Active Event Exclusive Consumption:**
   * Candies **can ONLY be eaten while an active piñata event is ongoing** on the server.
   * If a player attempts to consume an event candy after the battle ends, the action is cancelled with a message.

2. **Available Candy Types:**
   * 🍬 **Sugar Rush Candy:** Grants Speed II and Jump Boost to dodge shockwaves.
   * 🍫 **Regen Treat:** Rapidly restores health after surviving rage lightning strikes.
   * 🍭 **Titan Strength Pop:** Enhances damage dealt to the piñata and guardian minions.

---

## 🧹 The Candy Sweeper Service (`CandySweeperService`)

To safeguard the server economy and eliminate candy hoarding or dupe exploits:
* **Automated Global Purge:** The exact moment a piñata event concludes (upon defeat or timer expiration), the `CandySweeperService` performs an instantaneous sweep across:
  * All online player main inventories.
  * All player EnderChests.
  * All dropped item entities on the ground in all worlds.

---

<div align="space-between">

[**← 06. Particle LOD & Runic Circles**](06-Particle-LOD-and-Runic-Circles.md) | [**08. Leaderboards GUI & Stats →**](08-Leaderboards-GUI-and-Stats.md)

</div>
