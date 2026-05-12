# 🌿 Boticario Digital · Plantas Medicinales de Puerto Rico

> **"Preservar es honrar."**
> Un inventario vivo de las 101 plantas medicinales documentadas en Puerto Rico — donde el saber taíno, africano y español converge en código abierto.

**🔗 Demo en vivo:** [ricardojuanmorales.github.io/boticario-digital](https://ricardojuanmorales.github.io/boticario-digital/)

---

## ✨ ¿Por qué existe este proyecto?

Puerto Rico lleva siglos curándose con plantas. Ese conocimiento vive en las manos de abuelas, en solares de barrio y en la memoria oral de comunidades enteras — pero no en formato digital, accesible y libre. El **Boticario Digital** cambia eso.

Basado en el inventario académico **CIFI 4996** (Prof. Ricardo Juan Morales De Jesús, UPR 2022), este proyecto convierte 101 plantas medicinales en una herramienta educativa interactiva disponible para cualquiera con un navegador web.

---

## 🚀 Inicio rápido en 30 segundos

```bash
# 1. Clona el repositorio
git clone https://github.com/ricardojuanmorales/boticario-digital.git
cd boticario-digital

# 2. Levanta un servidor local (elige tu método preferido)
python3 -m http.server 8080      # Python 3 (macOS/Linux/Windows con Python)
npx serve .                      # Node.js
php -S localhost:8080            # PHP

# 3. Abre en tu navegador
# → http://localhost:8080
```

> ⚠️ **Nota:** El archivo `index.html` carga `plantas.json` via `fetch()`, por lo que necesitas un servidor local. No funcionará abriendo el archivo directamente con `file://`.

---

## 🖥️ Instrucciones de instalación por sistema operativo

### 🍎 macOS

```bash
# Opción 1 — Python (incluido en macOS)
git clone https://github.com/ricardojuanmorales/boticario-digital.git
cd boticario-digital
python3 -m http.server 8080
# Abre: http://localhost:8080

# Opción 2 — Node.js (si tienes npm instalado)
npx serve .
```

### 🪟 Windows

```powershell
# Opción 1 — Python (descarga desde python.org si no lo tienes)
git clone https://github.com/ricardojuanmorales/boticario-digital.git
cd boticario-digital
python -m http.server 8080
# Abre en Chrome/Firefox: http://localhost:8080

# Opción 2 — Node.js
npx serve .

# Opción 3 — Live Server en VS Code
# Abre la carpeta en VS Code → clic derecho en index.html → "Open with Live Server"
```

### 🐧 Linux

```bash
# Opción 1 — Python
git clone https://github.com/ricardojuanmorales/boticario-digital.git
cd boticario-digital
python3 -m http.server 8080

# Opción 2 — Node.js
npx serve .

# Opción 3 — nginx (producción)
sudo cp -r . /var/www/html/boticario-digital
sudo nginx -s reload
```

---

## ⭐ Características principales

| Característica | Detalle |
|---|---|
| 🌱 **101 plantas medicinales** | 48 familias botánicas · 436 indicaciones médicas |
| 📋 **4 vistas por planta** | Tradición · Botánica · Fitoquímica · Uso Práctico |
| ⚗️ **202 preparaciones** | Infusión · Decocción · Cataplasma · Baño · Tintura y más |
| 🔴🟡🟢 **Sistema de seguridad** | 3 niveles de riesgo con advertencias específicas |
| 📷 **15 plantas MVP** | Fotografías CC y fichas completas al 97% promedio |
| 🔬 **Fitoquímica completa** | Compuestos bioactivos con clase química y mecanismo de acción |
| 📖 **Glosario de 40 términos** | Fitoquímica · Botánica · Sistemas médicos · Seguridad |
| 🔍 **Búsqueda inteligente** | Normaliza acentos · 11 filtros por sistema corporal |
| 📱 **Diseño responsivo** | Móvil · Tablet · Escritorio |
| 🚫 **Sin instalación** | Standalone HTML + JSON · No requiere servidor en producción |

---

## 🗂️ Estructura del repositorio

```
boticario-digital/
├── index.html                          # Aplicación web principal
├── plantas.json                        # Base de datos — 101 plantas
├── boticario_101_plantas_completo.json # Fuente canónica completa (desarrollo)
├── Boticario_Digital_MVP_HTML_Full.html # Versión MVP standalone anterior
├── DOCUMENTACION.md                    # Documentación técnica completa
├── CIERRE_DE_SESION.md                 # Acta formal de sesión de trabajo
└── README.md                           # Este archivo
```

---

## 🧱 Stack tecnológico

| Capa | Tecnología |
|---|---|
| Interfaz | HTML5 semántico · CSS3 con Custom Properties |
| Lógica | JavaScript ES6+ (Vanilla, sin frameworks) |
| Datos | JSON estructurado (25+ campos por planta) |
| Tipografía | Crimson Pro · Lora · IBM Plex Mono (Google Fonts) |
| Imágenes | Wikimedia Commons (CC BY-SA 3.0 / 4.0) |
| Despliegue | GitHub Pages (estático) |

---

## 🌡️ Tabla de compatibilidad

| Navegador | Versión mínima | Estado |
|---|---|---|
| Chrome / Chromium | 88+ | ✅ Totalmente compatible |
| Firefox | 85+ | ✅ Totalmente compatible |
| Safari | 14+ | ✅ Totalmente compatible |
| Edge (Chromium) | 88+ | ✅ Totalmente compatible |
| Safari iOS | 14+ | ✅ Totalmente compatible |
| Chrome Android | 88+ | ✅ Totalmente compatible |
| IE 11 | — | ❌ No soportado |

**Requisitos de red:** La aplicación carga fuentes de Google Fonts y fotos de Wikimedia Commons. Para uso offline completo, se recomienda descargar las fuentes localmente.

---

## 🤝 Guía para contribuir

¡Las contribuciones son bienvenidas! Hay tres áreas prioritarias:

### 📝 Enriquecer datos de plantas

1. Abre `plantas.json`
2. Localiza la planta por `id`
3. Completa campos vacíos siguiendo el [schema documentado](DOCUMENTACION.md#esquema-de-datos)
4. Crea un Pull Request con descripción de las fuentes usadas

### 🐛 Reportar errores

Abre un [Issue en GitHub](https://github.com/ricardojuanmorales/boticario-digital/issues) con:
- Descripción del problema
- Pasos para reproducirlo
- Captura de pantalla (si aplica)
- Navegador y sistema operativo

### 💡 Proponer funcionalidades

Primero [abre un Issue](https://github.com/ricardojuanmorales/boticario-digital/issues) describiendo la idea antes de implementarla. Las funcionalidades deben alinearse con la misión educativa del proyecto.

### Flujo de trabajo estándar

```bash
git checkout -b feature/nombre-de-la-feature
# ... haz tus cambios ...
git add <archivos-específicos>
git commit -m "feat: descripción breve del cambio"
git push origin feature/nombre-de-la-feature
# Abre Pull Request en GitHub
```

---

## 🗺️ Hoja de ruta

- [ ] **Oleada 3** — Enriquecer historia cultural, compuestos y preparaciones de las 86 plantas restantes
- [ ] **Oleada 4** — Fotografías para las 86 plantas restantes (Wikimedia Commons / iNaturalist)
- [ ] **Separación HTML + JSON** — Migrar a arquitectura desacoplada
- [ ] **Mapa de distribución** — Visualización geográfica por municipio
- [ ] **Modo PWA offline** — Funcionalidad sin conexión para comunidades rurales
- [ ] **Versión en inglés** — Mismo JSON, interfaz traducida

---

## ⚕️ Aviso médico

> Esta herramienta es de carácter **educativo exclusivamente** y **no sustituye** diagnóstico, tratamiento ni consulta médica profesional. Consulta siempre a un profesional de salud antes de usar plantas medicinales.

---

## 📜 Licencia y créditos

**Código:** [MIT License](LICENSE)

**Datos:** Inventario de Plantas Medicinales para Puerto Rico — Prof. Ricardo Juan Morales De Jesús (CIFI 4996, UPR, 2022). Reproducidos con fines educativos.

**Fotografías:** [Wikimedia Commons](https://commons.wikimedia.org) bajo licencias Creative Commons (CC BY-SA 3.0 / CC BY-SA 4.0 / Dominio Público). Créditos individuales en cada ficha.

**Desarrollo digital:** Desarrollado con asistencia de **Claude Sonnet 4.5** (Anthropic) bajo supervisión y dirección del equipo del proyecto.

---

*🌿 Proyecto desarrollado en Puerto Rico · 2026*
*Universidad de Puerto Rico · Curso ESGE 4995*
