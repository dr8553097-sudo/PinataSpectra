# 🦄 03. Modelos 3D & Físicas de Balanceo

PinataSpectra recrea la sensación realista de golpear una piñata tradicional en el mundo real mediante cálculos de física armónica sobre Display Entities.

---

## 📐 1. Físicas de Suspensión por Cuerda (Catenary & Pendulum)

Cada piñata activa se suspende de un punto de anclaje en el techo o en el aire:
* **Balanceo Armónico:** Movimiento sinusoidal suave continuo simulando corrientes de viento.
* **Vector de Impulso de Impacto:** Cuando un jugador golpea la piñata, se calcula el vector direccional del golpe y se aplica un impulso cinético angular, haciendo que la piñata retroceda y se balancee en el ángulo exacto del impacto.
* **Cuerda de Partículas:** Una línea de partículas tensa conecta el punto de anclaje con la parte superior de la piñata, recalculando su curvatura en cada tick.

---

## 🎭 2. Morphing Dinámico de Expresiones Emocionales

A medida que la piñata pierde salud durante el evento, su cabeza y rostro cambian dinámicamente de textura o material para reflejar su estado emocional:

```
[100% - 75% HP]  😊 ESTADO: CALM (Tranquila, bailando)
       ↓
[75% - 50% HP]   😰 ESTADO: NERVOUS (Nerviosa, balanceo más rápido)
       ↓
[50% - 25% HP]   😡 ESTADO: ANGRY / ENRAGED (Furia, aura de fuego y rayos)
       ↓
[25% - 0% HP]    💀 ESTADO: DYING (A punto de romperse, rotación acelerada)
```

---

<div align="space-between">

[**← 02. Instalación**](02-Instalacion-y-Requisitos.md) | [**04. Máquina de Fases & Combate →**](04-Maquina-de-Fases-Combate.md)

</div>
