# ⚙️ 02. Installation & System Requirements

---

## 📋 System Requirements

* **Java Environment:** Java 21 or Java 25 (OpenJDK / Eclipse Temurin / GraalVM).
* **Server Software:** PaperMC, Purpur, or Spigot (Minecraft 1.20.1, 1.20.4, 1.20.6, 1.21.x, 1.26+).
* **Network Compatibility:** Standalone Paper servers, BungeeCord, and Velocity networks.

> [!NOTE]
> For optimal multithreaded tick stability, **Paper 1.21.x+** or **Purpur** is strongly recommended.

---

## 🔌 Hook Integrations

| Hook | Type | Purpose |
|---|---|---|
| [**PlaceholderAPI**](https://www.spigotmc.org/resources/placeholderapi.6245/) | Optional | Exposes real-time variables for scoreboards, tablists, and custom chat formats. |
| [**DecentHolograms**](https://www.spigotmc.org/resources/decentholograms.96927/) | Optional | Renders floating boss healthbars, active phase indicators, and damage popups. |
| [**Vault**](https://www.spigotmc.org/resources/vault.34315/) | Optional | Enables automatic in-game economy monetary payouts upon boss defeat. |
| **ModelEngine / Oraxen / ItemsAdder** | Optional | Allows using custom 3D entity models and items as piñatas or bats. |

---

## 🚀 Step-by-Step Installation

1. Download `PinataSpectra-1.0.0-RELEASE-pro.jar`.
2. Place the `.jar` file into your server's `/plugins/` directory.
3. Start or restart your server.
4. The plugin will generate the configuration directory `/plugins/PinataSpectra/` containing:
   * `config.yml` (Core settings, storage, particle LOD, and scheduler).
   * `pinatas.yml` (Piñata definitions, models, emotions, and phase mechanics).
   * `drops.yml` (Loot drop tables, item chances, and console commands).
   * `messages.yml` (Translatable message bundle with Hex & MiniMessage support).

---

<div align="space-between">

[**← 01. Architecture & Performance**](01-Architecture-and-Performance.md) | [**03. 3D Display Entities & Physics →**](03-3D-Display-Entities-and-Physics.md)

</div>
