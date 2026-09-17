# 🔮 06. Particle Engine, LOD Limits & Compatible Effects

PinataSpectra features a high-performance visual particle subsystem designed to maintain 60+ FPS on clients during intense 80+ player boss fights.

---

## ⚡ 1. Particle Engine Limits & Capacity

| Capacity Metric | Threshold Limit | Behavior Under Load |
|---|---|---|
| **Max Concurrent Particles** | 120 per server tick | Culls low-priority decorative sparks automatically |
| **Max Distance Radius** | 48.0 blocks | Entities beyond 48 blocks receive 0 particle packets |
| **Hit Popup Lifetime** | 20 ticks (1.0 second) | Smooth upward vertical interpolation |
| **Runic Circle Points** | 36 angular vertices | Dynamic step resolution (10° per vertex) |
| **Rope Vertex Density** | 1 particle per 0.4 blocks | Catenary spline calculation |

---

## 🎨 2. Supported Minecraft Particle Types

The runic circle and phase aura engines natively support all Spigot/Paper particle enums:

```yaml
# Recommended High-Visibility Particles:
- PORTAL           # Mystical purple/magenta vortex particles
- ENCHANT          # Floating galactic glyph runes
- SOUL_FIRE_FLAME  # Electric cyan flames (ideal for Phase 2 Shields)
- FLAME            # Warm orange embers (ideal for Phase 3 Rage)
- DRAGON_BREATH    # Volumetric purple boss clouds
- END_ROD          # Clean white sparkle highlights
- GLOW             # Bright glowing luminescent dust
- HEART            # Festive celebration hearts
- NOTE             # Musical score notes
- TOTEM_OF_UNDYING # Golden celebratory climax sparks
```

---

## 🔮 3. Performance Tuning Guide for 80+ Player Servers

If hosting massive community festivals with 80+ concurrent attackers:
1. **Set `particle-lod.close-distance: 6.0`** to concentrate particle density strictly around immediate melee attackers.
2. **Enable `particle-lod.enabled: true`** in `config.yml`.
3. **Use `PORTAL` or `ENCHANT`** for runic circles as they generate clean single-particle packets with low GPU rasterization overhead.

---

<div align="space-between">

[**← 05. Creating Custom Piñatas**](05-Creating-Custom-Pinatas.md) | [**07. Ephemeral Candies & Sweeper →**](07-Ephemeral-Candies-and-Sweeper.md)

</div>
