# ⚔️ 04. Combat Phases & Boss Mechanics

Combat in PinataSpectra is governed by a deterministic state machine (`PinataPhaseStateMachine`) that transforms the event into an interactive multi-stage boss fight.

---

## 🛡️ The 4 Combat Stages

### 🟢 Phase 1: Calm & Opening Encounter (100% → 75% HP)
* The piñata floats calmly, playing festive melodies and reacting with humorous or defiant dialogue in chat when struck.

### 🔵 Phase 2: Magical Shield & Minion Guardians (75% → 50% HP)
* **Orbital Absorption Shield:** An orbital energy shield of cyan particles surrounds the piñata. In this state, the boss is **100% immune to direct attacks**.
* **Guardian Minions:** Invocates 3 to 5 mini-piñata guardians. Players must defeat all guardian minions to shatter the shield and expose the main boss.

### 🔴 Phase 3: Enraged Frenzy & Shockwaves (50% → 25% HP)
* The piñata enters an enraged frenzy, displaying a fire and lava particle aura.
* **Knockback Shockwaves:** Periodically releases outward kinetic pulses that push nearby players away, accompanied by visual lightning strikes.

### 🟣 Phase 4: Final Stand & Loot Explosion (25% → 0% HP)
* Rapid rotation and dramatic soundtrack escalation.
* **Progressive Loot Detonation:** Upon reaching 0 HP, the piñata explodes into multi-colored fireworks, scattering custom loot tables, economy rewards, and ephemeral candies across the arena.

---

<div align="space-between">

[**← 03. 3D Display Entities & Physics**](03-3D-Display-Entities-and-Physics.md) | [**05. Creating Custom Piñatas →**](05-Creating-Custom-Pinatas.md)

</div>
