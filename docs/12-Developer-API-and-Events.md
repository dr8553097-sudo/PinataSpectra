# 💻 12. Developer API, Custom Events & Best Practices

PinataSpectra Sovereign Edition exposes an extensible Java API with custom Bukkit/Paper event listeners for server developers.

---

## 📦 1. Maven Dependency Configuration

```xml
<dependency>
    <groupId>net.dafealru</groupId>
    <artifactId>PinataSpectra</artifactId>
    <version>1.0.0-RELEASE</version>
    <scope>provided</scope>
</dependency>
```

---

## 🛠️ 2. Core API Methods

```java
import net.dafealru.pinataspectra.PinataSpectra;
import net.dafealru.pinataspectra.pinata.PinataInstance;
import net.dafealru.pinataspectra.pinata.PinataType;
import org.bukkit.Location;

public class MyPluginHook {

    private final PinataSpectra pinataAPI = PinataSpectra.getInstance();

    public void spawnCustomEvent(Location location) {
        // Spawn a tier 2 piñata programmatically
        pinataAPI.getPinataManager().spawnPinata("default", "tier_2", location);
    }

    public void inspectActiveBosses() {
        for (PinataInstance pinata : pinataAPI.getPinataManager().getActivePinatas().values()) {
            double hpPercent = pinata.getHealthPercent();
            int currentPhase = pinata.getStateMachine().getCurrentPhase();
            System.out.println("Active Pinata: " + pinata.getId() + " | Phase: " + currentPhase + " | HP: " + hpPercent + "%");
        }
    }
}
```

---

## 🎯 3. Custom Bukkit Event Listeners

PinataSpectra fires the following custom events throughout a piñata's lifecycle:

| Event Class | Description | Cancellable |
|---|---|:---:|
| `PinataSpawnEvent` | Dispatched when a new 3D Piñata is summoned | ✅ Yes |
| `PinataDamageEvent` | Fired when a player hits the piñata interaction hitbox | ✅ Yes |
| `PinataPhaseChangeEvent`| Fired when transitioning between Combat Phases (1 → 4) | ❌ No |
| `PinataBreakEvent` | Fired when the final hit destroys the piñata | ❌ No |
| `CandyConsumeEvent` | Fired when an ephemeral combat candy is eaten | ✅ Yes |

### Example Event Listener:
```java
import org.bukkit.event.EventHandler;
import org.bukkit.event.Listener;

public class PinataEventListener implements Listener {

    @EventHandler
    public void onPinataDamage(PinataDamageEvent event) {
        Player player = event.getPlayer();
        double damage = event.getDamage();
        
        // Custom bonus rewards or clan war points
        if (event.isCriticalHit()) {
            player.sendMessage("§a★ Critical Strike on the Piñata! §7(+" + damage + " dmg)");
        }
    }
}
```

---

## ⚠️ Security Best Practices

1. **Thread Safety:** Never invoke synchronous world modifications inside asynchronous database callbacks. Use `Bukkit.getScheduler().runTask(plugin, ...)` when modifying blocks or entity states from async threads.
2. **Database Integrity:** Do NOT edit the `database.db` SQLite file with external database tools while the server is active to prevent database lockups.
3. **Hot Reloads:** `/pinata reload` is 100% thread-safe and can be run in production without restarting the server or interrupting active combat encounters.

---

<div align="space-between">

[**← 11. Commands & Placeholders**](11-Commands-Permissions-and-Placeholders.md) | [**13. Edition Comparison (Lite vs Pro) →**](13-Comparison-and-Editions.md)

</div>
