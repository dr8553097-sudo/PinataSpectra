# 🧩 11. Commands, Permissions & PlaceholderAPI Reference

---

## 📜 Commands & Permissions Reference

| Command | Permission | Description |
|---|---|---|
| `/pinata spawn <type> [tier]` | `pinataspectra.admin` | Spawns a 3D Piñata at your target location |
| `/pinata top` | `pinataspectra.player` | Opens the 54-slot Interactive Top Leaderboard GUI |
| `/pinata killall` | `pinataspectra.admin` | Instantly removes all active Piñatas and cleans entities |
| `/pinata vote add <amount>` | `pinataspectra.admin` | Adds votes towards the Community Vote Goal |
| `/pinata vote set <amount>` | `pinataspectra.admin` | Sets the exact current vote count |
| `/pinata scheduler toggle` | `pinataspectra.admin` | Toggles or pauses the timed auto-scheduler |
| `/pinata sweepcandies` | `pinataspectra.admin` | Manually triggers the global Candy Sweeper purge |
| `/pinata reload` | `pinataspectra.admin` | Hot-reloads all YAML configuration and message files |

---

## 🧩 PlaceholderAPI Placeholders

| Placeholder | Description |
|---|---|
| `%pinataspectra_active_count%` | Number of currently active Piñatas in all worlds |
| `%pinataspectra_vote_current%` | Current votes accumulated towards the next Vote Party |
| `%pinataspectra_vote_required%` | Target votes required to trigger a Vote Party |
| `%pinataspectra_vote_percent%` | Progress percentage of the Vote Party goal (e.g., `80%`) |
| `%pinataspectra_scheduler_time%` | Formatted countdown until the next scheduled Piñata |
| `%pinataspectra_top_damage_1_name%` | Player name with highest total damage dealt |
| `%pinataspectra_top_damage_1_value%`| Total damage points of #1 damage dealer |
| `%pinataspectra_top_broken_1_name%` | Player name with most Piñatas destroyed (MVP #1) |
| `%pinataspectra_top_candies_1_name%`| Player name with most event candies consumed (#1) |

---

<div align="space-between">

[**← 10. Master Configuration Reference**](10-Master-Configuration-Reference.md) | [**12. Developer API & Best Practices →**](12-Developer-API-and-Events.md)

</div>
