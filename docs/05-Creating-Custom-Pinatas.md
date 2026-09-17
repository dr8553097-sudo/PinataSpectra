# 🛠️ 05. Step-by-Step Guide: Creating Custom Piñatas

Creating custom piñatas with unique 3D models, health bars, phase transitions, and loot tables is 100% configurable in `pinatas.yml`.

---

## 📝 Complete Example: `celestial_unicorn`

Add the following block to `/plugins/PinataSpectra/pinatas.yml`:

```yaml
pinatas:
  celestial_unicorn:
    display-name: "<gradient:#00f0ff:#a855f7><bold>🦄 CELESTIAL UNICORN PIÑATA</bold></gradient>"
    shape: "UNICORN"              # DONKEY, LLAMA, UNICORN, STAR, CUSTOM
    animation-style: "SINUSOIDAL" # SINUSOIDAL, CIRCULAR, CHAOTIC, BOUNCY
    base-health: 2000.0           # Total hitpoints
    hitbox-size: 2.0              # Interaction radius in blocks
    
    # 3D Model Properties
    model:
      material: "PLAYER_HEAD"
      custom-model-data: 0        # Optional (for custom resource pack models)
      head-texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTRmMGNmNzA4MGY2ZDFkYTUxMDYzOWU5MjU5Zjg3M2M1OTk5ZTRmYTRjNjQ2ZDAwNzM5ODZlYjExNTM5MmY5YSJ9fX0="
      scale:
        x: 2.5
        y: 2.5
        z: 2.5
        
    # Dynamic Emotion Textures
    emotions:
      calm:
        texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTRmMGNmNzA4MGY2ZDFkYTUxMDYzOWU5MjU5Zjg3M2M1OTk5ZTRmYTRjNjQ2ZDAwNzM5ODZlYjExNTM5MmY5YSJ9fX0="
      angry:
        texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMWQ3OTExY2M1ZWY5M2RlMTg2YmNjNDYxYTk2YWRhMTRhYzg1ZTIwMjI0MmYxNTc5NWE2OTlmM2Q0NTllNDM3YSJ9fX0="
        
    # Phase Combat Mechanics
    phases:
      phase_2:
        shield-health: 400.0
        minions-count: 5
        minion-type: "mini_unicorn"
      phase_3:
        knockback-power: 2.2
        lightning-strike: true
        
    # Rewards
    loot-table: "celestial_drops"
    candy-drop-count: 16
```

---

## 🔍 Key Configuration Options

1. **`shape`:** Core model archetype (`DONKEY`, `LLAMA`, `UNICORN`, `STAR`, `CUSTOM`).
2. **`animation-style`:**
   * `SINUSOIDAL`: Smooth realistic pendulum sway.
   * `CIRCULAR`: Orbital rotational path with vertical bobbing.
   * `BOUNCY`: Elastic vertical spring bounce.
   * `CHAOTIC`: High-energy unpredictable frenzy movements.
3. **`base-health`:** Total damage required to defeat the piñata. Multiplied by tier settings (`tier_1`, `tier_2`, `tier_3`).
4. **`head-texture`:** Standard Base64 player head skin value, allowing infinite 3D designs without requiring client mods.

---

## 🎮 In-Game Testing

Reload the plugin and spawn your custom piñata:
```bash
/pinata reload
/pinata spawn celestial_unicorn tier_1
```

---

<div align="space-between">

[**← 04. Combat Phases & Boss Mechanics**](04-Combat-Phases-and-Boss-Mechanics.md) | [**06. Particle LOD & Runic Circles →**](06-Particle-LOD-and-Runic-Circles.md)

</div>
