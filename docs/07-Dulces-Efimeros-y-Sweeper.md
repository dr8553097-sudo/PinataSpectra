# 🍬 07. Sistema de Dulces Efímeros & Candy Sweeper

Los **Dulces Efímeros (Ephemeral Candies)** son consumibles especiales que caen durante las fases de combate de la piñata para otorgar ventajas tácticas a los jugadores.

---

## 📜 Reglas de los Dulces

1. **Uso Exclusivo en Eventos Activos:**
   * Los dulces **SOLO pueden ser consumidos mientras haya al menos una piñata activa** en el servidor.
   * Si un jugador intenta comer un dulce fuera de un evento, el plugin cancela la acción y le informa mediante un mensaje de advertencia.

2. **Tipos de Dulces y Efectos:**
   * 🍬 **Caramelo de Velocidad (Sugar Rush):** Otorga Speed II y salto aumentado para esquivar ondas de choque.
   * 🍫 **Chocolate de Regeneración (Regen Treat):** Regenera salud rápidamente tras recibir daño de furia.
   * 🍭 **Paleta de Fuerza Titánica (Strength Pop):** Aumenta el daño infligido a la piñata y a los esbirros guardianes.

---

## 🧹 El Servicio Candy Sweeper (`CandySweeperService`)

Para proteger la economía del servidor y evitar que los jugadores acaparen o dupliquen dulces fuera del evento:
* **Purga Global Automática:** En cuanto la piñata finaliza (por ser destruida con éxito o por tiempo expirado), el servicio `CandySweeperService` barre y elimina de forma instantánea:
  * Todos los inventarios de los jugadores conectados.
  * Los inventarios de los EnderChests.
  * Todas las entidades de caramelos tiradas en el suelo del mundo.

---

<div align="space-between">

[**← 06. LOD & Círculo Rúnico**](06-LOD-Particulas-y-Optimizacion.md) | [**08. Leaderboards GUI 54-Slots →**](08-Leaderboards-GUI-Top.md)

</div>
