# ⚔️ 04. Máquina de Fases & Combate Boss

El combate en PinataSpectra está orquestado por una máquina de estados determinista (`PinataPhaseStateMachine`) que transforma una simple piñata en un encuentro épico contra un Boss.

---

## 🛡️ Desglose de las 4 Fases de Combate

### 🟢 Fase 1: Calma & Encuentro Inicial (100% → 75% HP)
* La piñata flota tranquilamente, emitiendo notas musicales y partículas suaves.
* Responde con frases cómicas o desafiantes en el chat al recibir los primeros golpes.

### 🔵 Fase 2: Escudo Mágico & Esbirros Guardianes (75% → 50% HP)
* **Escudo de Absorción:** La piñata despliega un escudo mágico orbital de partículas cian. En este estado, la piñata es **completamente inmune al daño directo**.
* **Invocación de Mini-Piñatas Minions:** Aparecen 3 a 5 esbirros guardianes que deben ser derrotados por los jugadores para romper el escudo y volver a hacer vulnerable a la piñata principal.

### 🔴 Fase 3: Furia Desatada / Frenzy (50% → 25% HP)
* La piñata entra en estado de cólera (*Enraged*), adquiriendo un aura de partículas de fuego y humo denso.
* **Pulsos de Retroceso (Knockback Waves):** Periódicamente emite ondas de choque sónicas que empujan a los jugadores cercanos y generan rayos visuales.

### 🟣 Fase 4: Gran Final & Lluvia Caótica (25% → 0% HP)
* La piñata gira a alta velocidad suspendida en el aire mientras suenan acordes de clímax musical.
* **Explosión Progresiva de Botín:** Al llegar a 0 HP, la piñata detona en un espectáculo de fuegos artificiales de colores, soltando el botín configurado en `drops.yml` y arrojando caramelos mágicos por todo el perímetro.

---

<div align="space-between">

[**← 03. Modelos 3D & Físicas**](03-Modelos-3D-y-Fisicas.md) | [**05. Guía: Cómo Crear una Piñata Custom →**](05-Guia-Como-Crear-una-Pinata.md)

</div>
