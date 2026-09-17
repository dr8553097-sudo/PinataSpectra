# 🛠️ 05. Guía Paso a Paso: Cómo Crear una Piñata Personalizada

Crear nuevas piñatas con apariencias, comportamientos y vidas personalizadas en PinataSpectra es extremadamente sencillo y 100% configurable mediante el archivo `pinatas.yml`.

---

## 📝 Estructura de una Piñata en `pinatas.yml`

A continuación, crearemos un ejemplo completo de una piñata legendaria llamada `dragon_festivo`:

```yaml
pinatas:
  dragon_festivo:
    display-name: "<gradient:#ff0055:#ffaa00><bold>🐉 PIÑATA DRAGÓN FESTIVO</bold></gradient>"
    shape: "DONKEY"               # DONKEY, LLAMA, UNICORN, STAR, CUSTOM
    animation-style: "SINUSOIDAL" # SINUSOIDAL, CIRCULAR, CHAOTIC, BOUNCY
    base-health: 1500.0           # Puntos de vida base
    hitbox-size: 1.8              # Radio de interacción en bloques
    
    # Modelo 3D (ItemDisplay)
    model:
      material: "PLAYER_HEAD"
      custom-model-data: 10402    # Opcional (si usas Resource Pack / Oraxen / ItemsAdder)
      head-texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTRmMGNmNzA4MGY2ZDFkYTUxMDYzOWU5MjU5Zjg3M2M1OTk5ZTRmYTRjNjQ2ZDAwNzM5ODZlYjExNTM5MmY5YSJ9fX0="
      scale:
        x: 2.2
        y: 2.2
        z: 2.2
        
    # Estados de Emoción & Texturas
    emotions:
      calm:
        texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMTRmMGNmNzA4MGY2ZDFkYTUxMDYzOWU5MjU5Zjg3M2M1OTk5ZTRmYTRjNjQ2ZDAwNzM5ODZlYjExNTM5MmY5YSJ9fX0="
      angry:
        texture: "eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMWQ3OTExY2M1ZWY5M2RlMTg2YmNjNDYxYTk2YWRhMTRhYzg1ZTIwMjI0MmYxNTc5NWE2OTlmM2Q0NTllNDM3YSJ9fX0="
        
    # Ajustes de Fases y Combate
    phases:
      phase_2:
        shield-health: 300.0
        minions-count: 4
        minion-type: "mini_dragon"
      phase_3:
        knockback-power: 1.8
        lightning-strike: true
        
    # Recompensas y Tabla de Botín
    loot-table: "dragon_legendary_drops"
    candy-drop-count: 12
```

---

## 🔍 Explicación de los Parámetros Clave

1. **`shape`:** El arquetipo de forma del cuerpo (soporta `DONKEY`, `LLAMA`, `UNICORN`, `STAR`, `CUSTOM`).
2. **`animation-style`:** El patrón matemático de balanceo:
   * `SINUSOIDAL`: Balanceo de péndulo suave.
   * `CIRCULAR`: Giro orbital con oscilación vertical.
   * `BOUNCY`: Rebote elástico vertical continuo.
   * `CHAOTIC`: Movimientos impredecibles de alta energía para fases de furia.
3. **`base-health`:** La vida total requerida para romperla. Puede escalarse automáticamente por el multiplicador del tier (`tier_1`, `tier_2`, `tier_3`).
4. **`head-texture`:** Valor Base64 de la cabeza de Minecraft que define la textura del modelo sin necesidad de mods.
5. **`scale`:** Escala tridimensional (`x`, `y`, `z`) para hacer la piñata gigante o pequeña.

---

## 🚀 Cómo Spawnear tu Nueva Piñata en el Juego

Una vez guardado el archivo `pinatas.yml`, recarga las configuraciones en el servidor:
```bash
/pinata reload
```
Y para spawnearla directamente donde estás mirando:
```bash
/pinata spawn dragon_festivo tier_1
```

---

<div align="space-between">

[**← 04. Fases & Combate**](04-Maquina-de-Fases-Combate.md) | [**06. LOD de Partículas & Anti-Lag →**](06-LOD-Particulas-y-Optimizacion.md)

</div>
