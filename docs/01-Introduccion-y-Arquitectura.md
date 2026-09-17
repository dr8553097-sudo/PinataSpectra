# 🏛️ 01. Introducción & Arquitectura de PinataSpectra

**PinataSpectra Sovereign Edition** fue concebido desde sus cimientos para resolver los problemas de rendimiento y rigidez que sufren los plugins tradicionales de piñatas y eventos comunitarios en Minecraft.

---

## ⚡ Principios de Diseño & Cero Lag

1. **Sin Entidades Pesadas de ArmorStands:**
   * En versiones antiguas de Minecraft, las animaciones 3D requerían docenas de ArmorStands invisibles con cabezas personalizadas, lo que causaba sobrecarga de paquetes en el cliente y saturación de entidades en el servidor.
   * PinataSpectra utiliza **`ItemDisplay` e `Interaction`** nativos de Minecraft 1.20 - 1.26+, reduciendo el costo de renderizado en un **85%**.

2. **Procesamiento Asíncrono de Operaciones I/O:**
   * Las consultas a base de datos (guardado de perfiles, ranking de daño, cálculo de top de dulces), notificaciones a Discord y purgas del inventario se ejecutan **fuera del hilo principal (Async)**.
   * Esto garantiza que el servidor mantenga **20.0 TPS sólidos** sin congelamientos (*micro-stutters*).

3. **Arquitectura Modular en Capas:**
   * **`PinataManager`:** Administra el ciclo de vida y la colección de piñatas activas en todos los mundos.
   * **`PinataPhaseStateMachine`:** Máquina de estados desacoplada que controla las transiciones de combate y emociones.
   * **`CandySweeperService`:** Servicio de seguridad que previene fugas de ítems y dupeos en la economía.
   * **`LeaderboardGUI`:** Interfaz gráfica interactiva de 54 slots con actualización asíncrona.

---

<div align="space-between">

[**← Inicio**](Home.md) | [**02. Instalación & Requisitos →**](02-Instalacion-y-Requisitos.md)

</div>
