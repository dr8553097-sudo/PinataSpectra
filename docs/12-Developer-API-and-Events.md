# 💻 12. Developer API & Security Best Practices

PinataSpectra exposes a clean Java API for custom server minigames and plugins.

---

## 🛠️ Java API Integration

```java
import net.dafealru.pinataspectra.PinataSpectra;
import net.dafealru.pinataspectra.pinata.PinataInstance;

// Access active plugin instance
PinataSpectra plugin = PinataSpectra.getInstance();

// Iterate through active piñatas
for (PinataInstance pinata : plugin.getPinataManager().getActivePinatas().values()) {
    UUID id = pinata.getId();
    double currentHealth = pinata.getCurrentHealth();
    int currentPhase = pinata.getStateMachine().getCurrentPhase();
    
    // Execute custom server logic
}
```

---

## ⚠️ Enterprise Best Practices & Warnings

1. **Database Safety:**
   * PinataSpectra utilizes asynchronous pooled connections (HikariCP). Never manually edit the `database.db` SQLite file with external database tools while the server is running to prevent database locks.
2. **Hot-Reloading in Production:**
   * `/pinata reload` is safe to run in production without destroying active piñatas or lagging the server.
3. **Economy Integrity:**
   * Always keep `candy-sweeper.enabled: true` in `config.yml` to ensure temporary combat candies do not persist after events.

---

<div align="space-between">

[**← 11. Commands & Placeholders**](11-Commands-Permissions-and-Placeholders.md) | [**13. Edition Comparison (Lite vs Pro) →**](13-Comparison-and-Editions.md)

</div>
