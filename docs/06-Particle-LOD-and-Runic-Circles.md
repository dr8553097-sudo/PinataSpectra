# 🔮 06. Particle LOD & Runic Ground Circles

When 50 to 80+ players gather in an arena to attack a piñata simultaneously, spawning hundreds of individual particles every tick can cause client-side FPS drops on lower-end systems. PinataSpectra features an intelligent **Level of Detail (LOD)** engine.

---

## ⚡ 1. How Particle LOD Operates

The engine computes player density and distance vectors:
* **Close Tier (< 8 blocks):** Full fidelity particle rendering (hit impacts, critical sparks, damage popups, and suspension rope).
* **Medium Tier (8 - 24 blocks):** 50% particle frequency reduction and secondary cosmetic particle culling.
* **Far Tier (> 24 blocks):** Displays only major boss boundary outlines and phase transition explosions.

---

## 🔮 2. Animated Runic Ground Circles

Beneath every suspended piñata, an animated runic circle projects directly onto the arena floor:
* **Perimeter Boundary:** Clearly demarcates the active combat hazard zone for players.
* **Continuous Rotation:** The circle smoothly rotates around the Y-axis using portal and enchantment particles.
* **Topographical Adaptation:** The ground detector calculates raycasts to project cleanly across stairs, slabs, and uneven terrain without floating artifacts.

---

<div align="space-between">

[**← 05. Creating Custom Piñatas**](05-Creating-Custom-Pinatas.md) | [**07. Ephemeral Candies & Sweeper →**](07-Ephemeral-Candies-and-Sweeper.md)

</div>
