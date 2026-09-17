# 🦄 03. 3D Display Entities & Suspension Physics

PinataSpectra uses vector mathematics and procedural kinematics on native `ItemDisplay` entities to recreate the physical sensation of striking a suspended piñata.

---

## 📐 1. Harmonic Catenary Rope Physics

When spawned, the piñata calculates an anchor point directly above it:
* **Harmonic Swaying:** Continuous sinusoidal bobbing and swaying simulating realistic air currents.
* **Kinetic Hit Impulses:** Each strike computes the attacker's look vector and applies an instantaneous angular velocity impulse. The piñata swings backwards in the direction of the hit before oscillating back to center.
* **Dynamic Particle Rope:** A procedural catenary particle line renders between the ceiling anchor and the piñata's top loop, updating its curvature each tick.

---

## 🎭 2. Dynamic Facial Emotion State Machine

As the piñata takes damage, its display texture morphs in real-time across four distinct emotional phases:

```
[100% - 75% HP]  😊 CALM     -> Content, dancing smoothly with musical notes.
       ↓
[75% - 50% HP]   😰 NERVOUS  -> Startled expressions, faster rotational swaying.
       ↓
[50% - 25% HP]   😡 ENRAGED  -> Fiery eyes, smoke aura, reactive knockback shockwaves.
       ↓
[25% - 0% HP]    💀 DYING    -> Panic rotation, cracking textures, preparing grand finale.
```

---

<div align="space-between">

[**← 02. Installation & Setup**](02-Installation-and-Setup.md) | [**04. Combat Phases & Boss Mechanics →**](04-Combat-Phases-and-Boss-Mechanics.md)

</div>
