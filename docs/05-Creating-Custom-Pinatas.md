# 🛠️ 05. Creating Custom Piñatas

PinataSpectra Sovereign features a modular YAML-based configuration architecture that allows server creators to design unique piñata bosses with custom 3D model data, drop tables, sound sets, and particle themes.

---

## 📁 File Structure

Custom piñata configurations are placed in the `/plugins/PinataSpectra/pinatas/` folder. Every file represents an independent boss tier.

<!-- tabs:start -->

#### **Infernal Dragon (`infernal_dragon.yml`)**
```yaml
id: "infernal_dragon"
display_name: "<gradient:#ff0055:#ffaa00><b>INFERNAL DRAGON PIÑATA</b></gradient>"
total_health: 500
damage_cap_per_hit: 5
hit_cooldown_ticks: 8

model:
  material: "STICK"
  custom_model_data: 10401
  scale: [2.2, 2.2, 2.2]
  billboard: "CENTER"

sound_profile:
  hit: "ENTITY_ENDER_DRAGON_HURT"
  shield_up: "BLOCK_BEACON_ACTIVATE"
  shield_break: "BLOCK_GLASS_BREAK"
  death: "ENTITY_ENDER_DRAGON_DEATH"

combat_phases:
  phase_2_minions:
    count: 4
    minion_health: 30
    minion_model_data: 10402
  phase_3_shockwave:
    interval_ticks: 100
    knockback_force: 2.5
    particle: "FLAME"

rewards:
  top_damager_commands:
    1:
      - "eco give %player% 50000"
      - "crate givekey %player% mythical 3"
      - "broadcast &6%player% achieved #1 MVP on Infernal Dragon!"
    2:
      - "eco give %player% 25000"
      - "crate givekey %player% mythical 1"
    3:
      - "eco give %player% 10000"
  per_hit_rewards:
    chance_percent: 45
    commands:
      - "eco give %player% 250"
```

#### **Cosmic Unicorn (`cosmic_unicorn.yml`)**
```yaml
id: "cosmic_unicorn"
display_name: "<gradient:#a855f7:#00f0ff><b>COSMIC UNICORN PIÑATA</b></gradient>"
total_health: 350
damage_cap_per_hit: 4
hit_cooldown_ticks: 10

model:
  material: "FEATHER"
  custom_model_data: 20101
  scale: [1.8, 1.8, 1.8]
  billboard: "VERTICAL"

sound_profile:
  hit: "ENTITY_ALLAY_HURT"
  shield_up: "BLOCK_AMETHYST_BLOCK_CHIME"
  shield_break: "BLOCK_AMETHYST_CLUSTER_BREAK"
  death: "UI_TOAST_CHALLENGE_COMPLETE"

combat_phases:
  phase_2_minions:
    count: 3
    minion_health: 20
    minion_model_data: 20102
  phase_3_shockwave:
    interval_ticks: 120
    knockback_force: 1.8
    particle: "END_ROD"

rewards:
  top_damager_commands:
    1:
      - "eco give %player% 30000"
      - "crate givekey %player% cosmic 2"
```
<!-- tabs:end -->

---

<div align="space-between">

[**← 04. Combat Phases & Boss Mechanics**](04-Combat-Phases-and-Boss-Mechanics.md) | [**06. Particle LOD & Runic Circles →**](06-Particle-LOD-and-Runic-Circles.md)

</div>