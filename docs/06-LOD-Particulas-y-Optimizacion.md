# 🔮 06. LOD de Partículas & Optimización Anti-Lag (80+ Jugadores)

Cuando se reúnen más de 50 o 80 jugadores en un mismo evento para golpear la piñata, renderizar partículas individuales por tick para cada jugador puede saturar los clientes con PCs de gama baja. PinataSpectra incorpora un motor **LOD (Level of Detail)** adaptativo.

---

## ⚡ 1. Cómo Funciona el Sistema LOD

El motor calcula la distancia euclidiana y la densidad de jugadores cercanos:
* **Jugadores a < 8 bloques:** Reciben el renderizado completo de partículas (efectos de golpe, chispas, números de daño y partículas de cuerda).
* **Jugadores a 8 - 24 bloques:** Se activa el nivel `LOD Medio` (se reduce la frecuencia de partículas en un 50% y se desactivan los popups secundarios).
* **Jugadores a > 24 bloques:** Se activa el nivel `LOD Bajo` (solo se renderiza el contorno del Boss y las explosiones de fase principales).

---

## 🔮 2. Círculo Rúnico en el Suelo (Runic Ground Circle)

Debajo de cada piñata suspendida en el aire, PinataSpectra proyecta un círculo rúnico animado sobre el suelo del arena:
* **Radio Dinámico:** Delimita visualmente el área de impacto y combate.
* **Rotación Angular Continua:** El círculo gira suavemente sobre el eje Y proyectando runas místicas (partículas de encantamiento y portal).
* **Adaptabilidad Topográfica:** El cálculo de altura se adapta automáticamente a desniveles del terreno para que las runas nunca queden flotando en el aire.

---

<div align="space-between">

[**← 05. Crear Piñata Custom**](05-Guia-Como-Crear-una-Pinata.md) | [**07. Dulces Efímeros & Sweeper →**](07-Dulces-Efimeros-y-Sweeper.md)

</div>
