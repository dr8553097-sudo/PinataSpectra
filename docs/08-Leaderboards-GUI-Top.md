# 🏆 08. Leaderboards GUI de 54 Slots (`/pinata top`)

PinataSpectra incluye un sistema de estadísticas persistentes y una interfaz gráfica interactiva de 54 casillas que permite a los jugadores consultar los rankings históricos del servidor.

---

## 📊 Categorías de Ranking

El menú `/pinata top` clasifica a los mejores jugadores en tres categorías principales:
1. 💥 **Top Damage (Mayores Dañadores):** Clasificación por puntos de daño total acumulado infligido a las piñatas.
2. 👑 **Top Broken / MVPs (Destructores de Piñatas):** Clasificación por cantidad de piñatas destruidas (último golpe / golpe de gracia).
3. 🍬 **Top Candies (Consumo de Dulces):** Clasificación por cantidad de caramelos efímeros consumidos durante los eventos.

---

## 🖥️ Características de la Interfaz GUI

* **Borde Animado de Vidrio:** Efecto visual de ondas de colores en los cristales del contorno.
* **Cabezas Personalizadas de Jugador:** Cada posición del Top 1 al 10 muestra la cabeza del jugador correspondiente con su skin, rango y puntuación exacta en el lore.
* **Carga Asíncrona:** El inventario se abre de inmediato y carga los datos desde SQLite/MySQL en un hilo secundario sin congelar al cliente.

---

<div align="space-between">

[**← 07. Dulces & Sweeper**](07-Dulces-Efimeros-y-Sweeper.md) | [**09. Auto-Scheduler & Metas de Votos →**](09-Auto-Scheduler-y-Vote-Party.md)

</div>
