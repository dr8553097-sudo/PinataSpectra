# ⚙️ 02. Instalación & Requisitos del Sistema

---

## 📋 Requisitos del Entorno

* **Java:** Java 21 o Java 25 (OpenJDK / GraalVM recomendado).
* **Servidor:** PaperMC, Purpur o Spigot (Minecraft 1.20.x, 1.21.x, hasta 1.26+).
* **Arquitecturas Compatibles:** Servidores tradicionales Paper y redes con BungeeCord/Velocity.

---

## 🔌 Integraciones Opcionales

| Plugin | Propósito | Beneficio |
|---|---|---|
| [**PlaceholderAPI**](https://www.spigotmc.org/resources/placeholderapi.6245/) | Integración de variables | Muestra cuentas regresivas, top de daño y metas de votos en tablists y scoreboards. |
| [**DecentHolograms**](https://www.spigotmc.org/resources/decentholograms.96927/) | Hologramas flotantes | Barras de vida flotantes y títulos 3D sobre la piñata. |
| [**Vault**](https://www.spigotmc.org/resources/vault.34315/) | Economía | Recompensas en dinero del servidor al dañar o romper la piñata. |
| **ModelEngine / Oraxen / ItemsAdder** | Modelos y texturas custom | Permite usar ítems y modelos personalizados como bates o piñatas especiales. |

---

## 🚀 Pasos de Instalación

1. Descargue el archivo compilado `PinataSpectra-1.0.0-RELEASE-pro.jar`.
2. Coloque el `.jar` en la carpeta `/plugins/` de su servidor.
3. Inicie o reinicie el servidor.
4. El plugin generará automáticamente las siguientes carpetas y archivos en `/plugins/PinataSpectra/`:
   * `config.yml` (Ajustes generales, base de datos, LOD de partículas, bates y scheduler).
   * `pinatas.yml` (Definición de modelos, vidas, fases y emociones de cada piñata).
   * `drops.yml` (Tablas de botín con probabilidades y comandos).
   * `messages.yml` (Todos los textos y traducciones personalizables con soporte de colores MiniMessage y Hex).

---

<div align="space-between">

[**← 01. Arquitectura**](01-Introduccion-y-Arquitectura.md) | [**03. Modelos 3D & Físicas →**](03-Modelos-3D-y-Fisicas.md)

</div>
