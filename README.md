# 🌿 Boticario Digital · Plantas Medicinales de Puerto Rico

> **"Preservar es honrar."**
> Un inventario vivo de las 101 plantas medicinales documentadas en Puerto Rico — donde el saber taíno, africano y español converge en código abierto.

**🔗 Demo en vivo:** [ricardojuanmorales.github.io/boticario-digital](https://ricardojuanmorales.github.io/boticario-digital/)

> 🧪 **Octubre 2026:** el Boticario evoluciona hacia la v1.0 con el **Framework Genérico V5.1** y la **Ficha de Saberes**. La app publicada sigue funcionando igual: sus archivos están en su lugar, y el MVP original queda congelado en la etiqueta [`v0.9.0-mvp-historico`](https://github.com/ricardojuanmorales/boticario-digital/tree/v0.9.0-mvp-historico).

---

## 🧭 Estado del proyecto · octubre 2026

| Componente | Estado |
|---|---|
| 🌐 App publicada (MVP) | ✅ Funciona en GitHub Pages; sus archivos siguen en la raíz, sin cambios. |
| 🧩 Framework Genérico V5.1 | ✅ Integrado en el repositorio (copia completa, con excepción registrada y revisada). Activado en modo INTEGRATE, nivel N3, con los lentes PH · IT · AT. |
| 📚 Ficha de Saberes | ✅ Spec v0.3 aprobada. Documento fundacional en **canon vigente**. Plantilla de uso lista. |
| 🌱 Primer caso: anamú (*Petiveria alliacea*) | ◐ Ficha v0.1 llena y validada (5 de 5 criterios). Activación por autorizar. |
| 🚦 Camino a la v1.0 | ◐ Quedan dos gates bloqueantes: G7 (ética y seguridad para menores) y G9 (calidad técnica). |

---

## ✨ ¿Por qué existe este proyecto?

Puerto Rico lleva siglos curándose con plantas. Ese conocimiento vive en las manos de abuelas, en solares de barrio y en la memoria oral de comunidades enteras — pero no en formato digital, accesible y libre. El **Boticario Digital** cambia eso.

Basado en el inventario académico **CIFI 4996** (Prof. Ricardo Juan Morales De Jesús, UPR 2022), este proyecto convierte 101 plantas medicinales en una herramienta educativa interactiva disponible para cualquiera con un navegador web.

El Boticario forma parte de un **ecosistema del buen vivir**: un grupo de aplicaciones *local-first* (Recetario, Yocahú, Wellbe, Índice, Tablero y el propio Boticario) que comparten el Framework V5.1 como forma de trabajo.

---

## 📚 La Ficha de Saberes

Es la ficha estandarizada de cada planta, y el corazón de la versión 1.0.

- **Cuatro niveles de saber** (inspirados en Max-Neef): empírico, pragmático, normativo y de valores.
- **Cinco voces:** la tradición taína y afrocaribeña, el Ayurveda, la medicina tradicional china, los saberes andinos e indígenas, y la biomedicina. Cada voz se registra en sus propios términos, **sin forzar equivalencias** entre ellas.
- **Activación proporcional:** cada especie activa solo los módulos que le corresponden; los demás quedan durmientes o se marcan como "no aplica".
- **Seguridad por audiencia:** cada ficha se muestra distinto a cuatro públicos (escolar, general, adulto e investigación). Un estudiante no ve dosis ni preparaciones, y toda dosis tradicional se rotula como "reportada, no validada".
- **Bienestar en 13 dimensiones**, para ubicar cada planta dentro de una vida buena y no solo frente a una enfermedad.

| Documento | Para qué sirve |
|---|---|
| [Documento fundacional](02_ARQUITECTURA_CONCEPTUAL/Arquitecturas_Referencia/2026-10-10_Documento_Fundacional_Ficha_de_Saberes_v1_0.md) | Qué es la ficha, de dónde viene y por qué está hecha así. **Empieza aquí.** |
| [Plantilla de uso v0.3](07_PLANTILLAS_Y_MODELOS/Plantillas_Documentos/2026-10-10_Plantilla_Ficha_de_Saberes_v0_3.md) | Para llenar una ficha nueva. |
| [Spec v0.3](00_CONTROL_MAESTRO/Spec_Driven_Development/2026-10-10_Auditoria_Triangulacion_y_Spec_Ficha_Saberes_FICHA_2_v0_3.md) | La especificación técnica completa, con sus reglas. |
| [Ficha del anamú v0.1](13_INVESTIGACION_Y_EVIDENCIA/Sintesis_Evidencia/2026-10-10_Ficha_Saberes_Petiveria_alliacea_Anamu_v0_1.md) | El primer caso aplicado, con 16 fuentes verificadas. |
| [Informe de validación](15_EVALUACION_CALIDAD_Y_AUDITORIA/Evidencias_Validacion/2026-10-10_Informe_Validacion_FICHA_3_Anamu_v0_1.md) | Cómo se probó la ficha con el anamú y qué se aprendió. |

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
>
> `index.html` sigue siendo la app del Boticario. La entrada del Framework está en `index_framework_v5_1_0.html`, renombrada para no sobrescribir la app.

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

## ⭐ Características principales (app publicada)

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
├── index.html                           # App del Boticario (MVP publicado)
├── plantas.json                         # Base de datos — 101 plantas
├── boticario_101_plantas_completo.json  # Fuente canónica completa (desarrollo)
├── Boticario_Digital_MVP_HTML_Full.html # Versión MVP standalone anterior
├── DOCUMENTACION.md / .pdf              # Documentación técnica del MVP
├── CIERRE_DE_SESION.md                  # Acta de la sesión del MVP (mayo 2026)
├── README.md                            # Este archivo
│
├── index_framework_v5_1_0.html          # Entrada del Framework (renombrada)
├── README_Framework_V5_1_0.md           # README del Framework (renombrado)
├── README_English.md                    # README del Framework en inglés (viene con el release)
├── 00_CONTROL_MAESTRO/ … 21_WIKI_DOCUMENTACION_HUMANA/
│                                        # Macroestructura del Framework V5.1
├── 99_ARCHIVO_HISTORICO/                # Archivo histórico
├── apps/framework-v5/                   # App del Framework
└── legacy/v4/                           # Versión anterior del Framework
```

**Dónde está el trabajo del Boticario dentro del Framework:**

| Cartapacio | Qué guarda |
|---|---|
| `00_CONTROL_MAESTRO/` | Specs, expediente portable, manifests y el prompt de activación |
| `02_ARQUITECTURA_CONCEPTUAL/` | El documento fundacional de la Ficha de Saberes |
| `03_METODOLOGIA_Y_FLUJO_DE_TRABAJO/` | La ficha de activación del proyecto |
| `04_GOBERNANZA_ETICA_Y_RIESGOS/` | Excepciones registradas |
| `07_PLANTILLAS_Y_MODELOS/` | La plantilla de la Ficha de Saberes |
| `13_INVESTIGACION_Y_EVIDENCIA/` | Las fichas de cada planta |
| `15_EVALUACION_CALIDAD_Y_AUDITORIA/` | Informes de validación |
| `18_DOCUMENTACION_ACTIVA/` | Decisiones, primer de continuidad, cierres de sesión y changelog |
| `21_WIKI_DOCUMENTACION_HUMANA/` | Guías para personas (pendientes para el Boticario) |

---

## 🔄 Cómo retomar el trabajo

Todo lo necesario para continuar vive en el repositorio. No hace falta ningún ZIP: una sesión nueva se activa **por referencia**.

1. **Prompt de activación:** [`00_CONTROL_MAESTRO/Prompts_Activacion/2026-10-10_Prompt_Activacion_Boticario_Digital_101_v1_0.md`](00_CONTROL_MAESTRO/Prompts_Activacion/2026-10-10_Prompt_Activacion_Boticario_Digital_101_v1_0.md) — pégalo al abrir una sesión con IA.
2. **Dónde estamos:** [primer de continuidad](18_DOCUMENTACION_ACTIVA/Primers_Continuidad/2026-10-10_Primer_Continuidad_Donde_Estamos_Boticario_v1_0.md).
3. **Por qué está así:** [registro maestro de decisiones](18_DOCUMENTACION_ACTIVA/Registro_Decisiones/2026-10-09_Registro_Maestro_Decisiones_Boticario_Digital_101_v1_0.md) (D-A01 a D-A30).
4. **Qué quedó pendiente:** [último cierre de sesión](18_DOCUMENTACION_ACTIVA/Cierres_Reportes/Cierres_Sesion/2026-10-10_Cierre_Sesion_Boticario_v1_0.md).

---

## 🧱 Stack tecnológico

| Capa | Tecnología |
|---|---|
| Interfaz | HTML5 semántico · CSS3 con Custom Properties |
| Lógica | JavaScript ES6+ (Vanilla, sin frameworks) |
| Datos | JSON estructurado (25+ campos por planta) |
| Tipografía | Crimson Pro · Lora · IBM Plex Mono (Google Fonts) |
| Imágenes | Wikimedia Commons (CC BY-SA 3.0 / 4.0) |
| Despliegue | GitHub Pages (estático), desde `main` |
| Gestión del proyecto | Framework Genérico V5.1 · desarrollo guiado por especificaciones (SDD) |

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

1. Para una planta nueva o una revisión a fondo, usa la [plantilla de la Ficha de Saberes](07_PLANTILLAS_Y_MODELOS/Plantillas_Documentos/2026-10-10_Plantilla_Ficha_de_Saberes_v0_3.md) y el [anamú](13_INVESTIGACION_Y_EVIDENCIA/Sintesis_Evidencia/2026-10-10_Ficha_Saberes_Petiveria_alliacea_Anamu_v0_1.md) como ejemplo.
2. Para correcciones puntuales en la app, abre `plantas.json`, localiza la planta por `id` y sigue el [schema documentado](DOCUMENTACION.md#esquema-de-datos).
3. Cita cada afirmación con su fuente y la fecha de búsqueda.
4. Crea un Pull Request con la descripción de las fuentes usadas.

> 🛡️ Todo PR que toque datos de plantas pasa por **revisión humana**, con atención especial a riesgos, contraindicaciones e interacciones, porque la audiencia incluye menores.

### 🐛 Reportar errores

Abre un [Issue en GitHub](https://github.com/ricardojuanmorales/boticario-digital/issues) con:
- Descripción del problema
- Pasos para reproducirlo
- Captura de pantalla (si aplica)
- Navegador y sistema operativo

### 💡 Proponer funcionalidades

Primero [abre un Issue](https://github.com/ricardojuanmorales/boticario-digital/issues) describiendo la idea antes de implementarla. Las funcionalidades deben alinearse con la misión educativa del proyecto.

### Flujo de trabajo estándar

`main` publica la app. Todo cambio entra por una rama y se integra con revisión humana.

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

### Hacia la v1.0

- [x] Instalar el Framework V5.1 como prototipo
- [x] Ficha de Saberes: spec v0.3, plantilla y documento fundacional
- [x] Primera ficha aplicada y validada: anamú
- [x] Integrar el Framework y la Ficha de Saberes en `main`, sin tocar la app publicada
- [ ] Autorizar la activación de la ficha del anamú
- [ ] Ficha de Saberes v1.0 (posible segundo caso: jengibre)
- [ ] JSON Schema para `plantas.json`, con validación automática
- [ ] Política de seguridad para menores (gate G7)
- [ ] Licencia del código y de los datos, y custodia de los saberes (gate G7)
- [ ] Seguridad y calidad del código de la app (gate G9)
- [ ] Wiki humana del Boticario

### Contenido (continúa del MVP)

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

**Código:** MIT, según las versiones anteriores de este README. El archivo `LICENSE` todavía no está en el repositorio; la licencia del código y de los datos de custodia está pendiente de decisión (gate G7).

**Datos:** Inventario de Plantas Medicinales para Puerto Rico — Prof. Ricardo Juan Morales De Jesús (CIFI 4996, UPR, 2022). Reproducidos con fines educativos.

**Ficha de Saberes:** Ricardo Juan Morales De Jesús y Guersom J. Báez Fonseca, coautores.

**Framework Genérico V5.1:** Ricardo Juan Morales De Jesús.

**Fotografías:** [Wikimedia Commons](https://commons.wikimedia.org) bajo licencias Creative Commons (CC BY-SA 3.0 / CC BY-SA 4.0 / Dominio Público). Créditos individuales en cada ficha.

**Desarrollo digital:** Desarrollado con asistencia de **Claude Sonnet 4.5** (MVP) y **Claude Opus 5.5** (Framework V5.1 y Ficha de Saberes), de Anthropic, bajo supervisión y dirección del equipo del proyecto.

---

*🌿 Proyecto desarrollado en Puerto Rico · 2026*
*Universidad de Puerto Rico · Curso ESGE 4995*
