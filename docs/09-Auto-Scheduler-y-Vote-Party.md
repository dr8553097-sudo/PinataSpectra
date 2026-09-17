# ⏳ 09. Auto-Scheduler & Metas de Votos Comunitarias

PinataSpectra automatiza la realización de eventos periódicos en tu servidor para mantener a tu comunidad activa sin necesidad de supervisión constante del staff.

---

## ⏰ 1. Motor de Eventos Automáticos (Auto-Scheduler Engine)

El motor `AutoSchedulerEngine` programa invocaciones automáticas cada cierto intervalo de tiempo (ej. cada 2 o 4 horas):
* **Avisos Previos con Cuenta Regresiva:** Envía mensajes de broadcast configurables (15 minutos antes, 5 minutos, 1 minuto y 30 segundos) alertando a los jugadores sobre la ubicación de la piñata.
* **Ubicaciones Múltiples:** Permite registrar coordenadas de arenas predeterminadas en diferentes mundos.

---

## 🗳️ 2. Meta Comunitaria de Votos (Vote Party / Donation Goal)

* **Compatibilidad Nativa con NuVotifier:** Detecta automáticamente los votos entrantes de los jugadores en páginas de votación de Minecraft.
* **BossBar Dinámica Global:** Muestra una barra de progreso en la parte superior de la pantalla indicando el progreso actual (ej. `[████████░░] 80/100 Votos para la Piñata Party`).
* **Activación de Fiesta:** En cuanto se alcanza la meta, se reproduce un sonido festivo para todo el servidor y se invoca la piñata comunitaria especial con botín incrementado.

---

<div align="space-between">

[**← 08. Leaderboard GUI Top**](08-Leaderboards-GUI-Top.md) | [**10. Configuración YAML Maestra →**](10-Configuracion-YAML-Maestra.md)

</div>
