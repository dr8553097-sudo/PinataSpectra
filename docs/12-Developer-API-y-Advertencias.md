# 💻 12. Developer API, Eventos & Advertencias Avanzadas

PinataSpectra expone una API Java modular para que desarrolladores puedan integrar piñatas en sus propios plugins y minijuegos.

---

## 🛠️ Cómo Usar la API en tu Plugin

Agrega la dependencia a tu `pom.xml` o archivo `build.gradle`:

```java
import net.dafealru.pinataspectra.PinataSpectra;
import net.dafealru.pinataspectra.pinata.PinataInstance;

// Obtener instancia del plugin
PinataSpectra api = PinataSpectra.getInstance();

// Consultar piñatas activas
for (PinataInstance pinata : api.getPinataManager().getActivePinatas().values()) {
    UUID pinataId = pinata.getId();
    double health = pinata.getCurrentHealth();
    int currentPhase = pinata.getStateMachine().getCurrentPhase();
    
    // Ejecutar lógica custom del servidor
}
```

---

## ⚠️ Advertencias de Seguridad & Buenas Prácticas

1. **Nunca modifiques el archivo de base de datos mientras el servidor esté encendido:**
   * PinataSpectra utiliza conexiones agrupadas asíncronas con HikariCP. Cualquier edición externa directa a `database.db` con el servidor activo puede provocar bloqueos de archivo en Windows/Linux.
2. **Uso de `/pinata reload` en Producción:**
   * El comando `/pinata reload` es completamente seguro y recarga todos los archivos `.yml` en caliente sin reiniciar el servidor ni destruir piñatas en combate.
3. **Protección Anti-Dupeo de Dulces:**
   * Asegúrate de mantener activada la opción `candy-sweeper.enabled: true` en `config.yml` para evitar que los jugadores almacenen caramelos de efectos temporales en cofres de otras dimensiones.

---

<div align="space-between">

[**← 11. Comandos, Permisos & Placeholders**](11-Comandos-Permisos-Placeholders.md) | [**Volver al Inicio (Home) 🏠**](Home.md)

</div>
