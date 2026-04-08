
# 🌿 Boticario Digital de Plantas Medicinales de Puerto Rico

Inventario digital interactivo de las 101 plantas medicinales documentadas en Puerto Rico por el Prof. Ricardo Juan Morales De Jesús en el marco del curso CIFI 4996 de la Universidad de Puerto Rico (2022). Implementación digital por el curso ESGE 4995 (2026). 

**Demo:** [Ver el Boticario Digital →](https://ricardojuanmorales.github.io/boticario-digital/)

---

## Sobre el proyecto

El Boticario Digital nace de la necesidad de preservar y hacer accesible el conocimiento herbolario de Puerto Rico — un patrimonio que fusiona tres tradiciones médicas: la taína, la africana y la española colonial. El inventario fuente, *CIFI 4996*, documenta 101 plantas con sus nombres, usos, preparaciones y propiedades, pero existe únicamente en formato académico impreso.

Este proyecto convierte ese inventario en una herramienta digital educativa, interactiva y de acceso libre, diseñada para estudiantes, profesionales de salud comunitaria, herbolarios y el público general de Puerto Rico.

> ⚕️ **Aviso:** Esta herramienta es de carácter educativo exclusivamente y no sustituye diagnóstico ni tratamiento médico profesional.

---

## Características

- **101 plantas medicinales** organizadas por sistema corporal, tipo, nivel de riesgo y completitud
- **Fichas detalladas** con 4 vistas: Tradición cultural, Botánica, Fitoquímica y Uso Práctico
- **116 preparaciones** paso a paso: infusiones, decocciones, cataplasmas, baños, jugos, aceites y tinturas
- **Sistema de seguridad** con 3 niveles de riesgo (🔴 alto · 🟡 moderado · 🟢 bajo) y advertencias específicas
- **Custodios del conocimiento** — reconocimiento de las tradiciones taína, africana, española y académica detrás de cada planta
- **Fotografías** de las 15 plantas MVP con licencia Creative Commons (Wikimedia Commons)
- **Claves de identificación** botánica visual para cada planta MVP
- **Compuestos bioactivos** con clase química y mecanismo de acción
- **Glosario** de 40 términos fitoquímicos, botánicos y culturales
- **Búsqueda** con normalización de acentos, 11 filtros por sistema corporal y ordenación múltiple
- **Diseño responsivo** — funciona en móvil, tablet y escritorio
- **Aplicación standalone** — un solo archivo HTML, sin dependencias de servidor ni instalación

---

## Estado del inventario — Versión 2.0

### Plantas MVP (15 plantas estrella)

| Campo | Estado |
|---|---|
| Completitud promedio | **97%** |
| Fotografías (Wikimedia Commons CC) | ✅ 15 / 15 |
| Custodios del conocimiento | ✅ 15 / 15 (2 por planta) |
| Preparaciones (≥ 2 por planta) | ✅ 15 / 15 |
| Compuestos bioactivos (≥ 3) | ✅ 15 / 15 |
| Claves de identificación (≥ 4) | ✅ 15 / 15 |
| Indicaciones medicinales (≥ 6) | ✅ 15 / 15 |
| Referencias bibliográficas (≥ 2) | ✅ 15 / 15 |
| Historia cultural específica | ✅ 15 / 15 |

**Plantas MVP:** Anamú · Canela · Cariaquito · Culantro del monte · Cundeamor · Guanábana · Guayabo · Jengibre dulce · Limoncillo · Malagueta · Manzanilla · Parcha · Romero · Sábila · Yerba buena

### Inventario completo (101 plantas)

| Grupo | Plantas | Completitud |
|---|---|---|
| MVP | 15 | 97% promedio |
| Restantes | 86 | 65% promedio |
| **Total** | **101** | **69% promedio** |

### Oleadas de enriquecimiento completadas

| Oleada | Descripción | Estado |
|---|---|---|
| 0 | Texto enriquecido MVP: 2ª preparación, indicaciones, historia, contraindicaciones, referencias | ✅ Completada |
| 1 | Fotografías MVP: Wikimedia Commons CC BY-SA | ✅ Completada |
| 2 | Custodios del conocimiento MVP: por tradición cultural | ✅ Completada |
| 3 | Texto enriquecido 86 plantas restantes | 🔄 Pendiente |
| 4 | Fotografías 86 plantas restantes | 🔄 Pendiente |

### Resumen estadístico

```
101 plantas · 48 familias botánicas · 436 indicaciones medicinales
116 preparaciones · 15 fotografías CC · 15 fichas de custodios
8 plantas de alto riesgo documentadas
```

---

## Fuente de datos

**Inventario de Plantas Medicinales para Puerto Rico**
Prof. Ricardo Juan Morales De Jesús — Universidad de Puerto Rico, 2022
Código de curso: CIFI 4996

Las fotografías son de [Wikimedia Commons](https://commons.wikimedia.org) bajo licencias Creative Commons (CC BY-SA 3.0 / CC BY-SA 4.0 / Dominio Público).

---

## Desarrollo con inteligencia artificial

Este proyecto fue desarrollado íntegramente con asistencia de **Claude Sonnet 4.5** de [Anthropic](https://anthropic.com), utilizando la interfaz conversacional de [Claude.ai](https://claude.ai).

### Rol de la IA en el proyecto

El proceso de desarrollo fue colaborativo y multidisciplinar. Claude participó en:

- **Arquitectura de datos** — diseño del schema JSON canónico con 30+ campos por planta
- **Extracción y estructuración** — procesamiento del PDF fuente (CIFI 4996, 122 páginas) en objetos JSON estructurados para las 101 plantas
- **Enriquecimiento editorial** — redacción de historias culturales, custodios del conocimiento, compuestos bioactivos con mecanismo de acción, claves de identificación botánica y preparaciones paso a paso, basados en literatura científica y etnobotánica del Caribe
- **Desarrollo frontend** — diseño e implementación del HTML/CSS/JS standalone, incluyendo sistema de filtros, modal de fichas, 4 vistas de información, diseño responsivo y sistema de seguridad
- **Investigación bibliográfica** — búsqueda y verificación de referencias de PubMed, Dr. Duke's Phytochemical DB y fuentes académicas del Caribe
- **Control de calidad** — auditoría sistemática de completitud campo por campo para las 101 plantas
- **Planificación estratégica** — diseño del sistema de oleadas de enriquecimiento incremental

### Modelo utilizado

| Parámetro | Valor |
|---|---|
| Modelo | Claude Sonnet 4.5 |
| Proveedor | Anthropic |
| Interfaz | Claude.ai (conversacional) |
| Periodo de desarrollo | Abril 2026 |

### Supervisión humana

Todo el contenido generado con IA fue revisado, dirigido y aprobado por el equipo del proyecto. Las decisiones editoriales, la selección de plantas MVP, la estrategia de custodios del conocimiento y los criterios de completitud fueron definidos por los autores humanos del proyecto. La IA actuó como herramienta de investigación, estructuración y desarrollo — no como autoridad en ninguna afirmación médica o cultural.

---

## Estructura del repositorio

```
boticario-digital/
├── index.html                          # Aplicación web completa (standalone)
├── README.md                           # Este archivo
└── boticario_101_plantas_completo.json # Fuente de datos canónica (uso futuro)
```

> **Nota técnica:** La versión actual (`index.html`) tiene los datos embebidos directamente en el JavaScript para funcionar como archivo standalone sin servidor. El JSON separado es la fuente canónica para futuras versiones y desarrollos.

---

## Hoja de ruta

- [ ] **Oleada 3** — Enriquecer las 86 plantas restantes: historia cultural, compuestos, preparaciones, custodios
- [ ] **Oleada 4** — Fotografías para las 86 plantas restantes (Wikimedia Commons / iNaturalist CC)
- [ ] **Separación HTML + JSON** — Migrar a arquitectura desacoplada al completar las oleadas
- [ ] **Mapa de distribución** — Visualización geográfica por municipio de Puerto Rico
- [ ] **Modo offline / PWA** — Funcionalidad sin conexión para uso en comunidades rurales
- [ ] **Versión en inglés** — Mismo JSON, HTML traducido

---

## Licencia

El código de esta aplicación está disponible bajo licencia [MIT](LICENSE).

Los datos del inventario de plantas provienen del trabajo académico del Prof. Ricardo Juan Morales De Jesús (CIFI 4996, UPR, 2022) y se reproducen con fines educativos.

Las fotografías son de Wikimedia Commons bajo sus respectivas licencias Creative Commons — los créditos específicos aparecen en cada ficha de planta dentro de la aplicación.

---

*Proyecto desarrollado en Puerto Rico · 2026*
*Con el apoyo de Claude AI (Anthropic) como herramienta de investigación y desarrollo*
