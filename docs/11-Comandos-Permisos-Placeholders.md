# 🧩 11. Comandos, Permisos & Placeholders de PlaceholderAPI

---

## 📜 Tabla de Comandos & Permisos

| Comando | Permiso | Descripción |
|---|---|---|
| `/pinata spawn <tipo> [tier]` | `pinataspectra.admin` | Invoca una piñata 3D en tu ubicación o en el bloque objetivo |
| `/pinata top` | `pinataspectra.player` | Abre el menú GUI interactivo de 54 casillas del Top |
| `/pinata killall` | `pinataspectra.admin` | Elimina todas las piñatas activas y limpia entidades |
| `/pinata vote add <cantidad>` | `pinataspectra.admin` | Suma votos al contador de la meta comunitaria |
| `/pinata vote set <cantidad>` | `pinataspectra.admin` | Establece el número exacto de votos actuales |
| `/pinata scheduler toggle` | `pinataspectra.admin` | Activa o pausa el motor de piñatas automáticas por tiempo |
| `/pinata sweepcandies` | `pinataspectra.admin` | Ejecuta manualmente la purga del barredor de dulces |
| `/pinata reload` | `pinataspectra.admin` | Recarga todas las configuraciones YAML sin reiniciar |

---

## 🧩 Placeholders Oficiales de PlaceholderAPI

| Placeholder | Descripción / Valor de Retorno |
|---|---|
| `%pinataspectra_active_count%` | Número de piñatas activas actualmente en el servidor |
| `%pinataspectra_vote_current%` | Votos acumulados hacia la próxima Vote Party |
| `%pinataspectra_vote_required%` | Votos necesarios para completar la meta |
| `%pinataspectra_vote_percent%` | Porcentaje de progreso de la meta comunitaria (ej. `75%`) |
| `%pinataspectra_scheduler_time%` | Cuenta regresiva formateada hasta la próxima piñata automática |
| `%pinataspectra_top_damage_1_name%` | Nombre del jugador en el puesto #1 de daño |
| `%pinataspectra_top_damage_1_value%` | Daño acumulado del jugador en el puesto #1 |
| `%pinataspectra_top_broken_1_name%` | Nombre del jugador con más piñatas destruidas (MVP #1) |
| `%pinataspectra_top_candies_1_name%` | Nombre del jugador con más dulces consumidos (#1) |

---

<div align="space-between">

[**← 10. Configuración YAML**](10-Configuracion-YAML-Maestra.md) | [**12. Developer API & Advertencias →**](12-Developer-API-y-Advertencias.md)

</div>
