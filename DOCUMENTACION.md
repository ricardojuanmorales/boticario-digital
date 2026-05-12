# Documentación Oficial — Boticario Digital de Plantas Medicinales de Puerto Rico

**Versión:** 2.0  
**Fecha:** 12 de mayo de 2026  
**Autor del inventario:** Prof. Ricardo Juan Morales De Jesús  
**Institución:** Universidad de Puerto Rico  
**Cursos:** CIFI 4996 (inventario fuente, 2022) · ESGE 4995 (implementación digital, 2026)

---

## Tabla de contenido

1. [Descripción general](#1-descripción-general)
2. [Fundamento conceptual](#2-fundamento-conceptual)
3. [Arquitectura técnica](#3-arquitectura-técnica)
4. [Estructura de archivos](#4-estructura-de-archivos)
5. [Funcionalidades y algoritmos](#5-funcionalidades-y-algoritmos)
6. [Esquema de datos](#6-esquema-de-datos)
7. [Funciones y métodos documentados](#7-funciones-y-métodos-documentados)
8. [Sistema de diseño](#8-sistema-de-diseño)
9. [Accesibilidad](#9-accesibilidad)
10. [Diseño responsivo](#10-diseño-responsivo)
11. [Guía de uso paso a paso](#11-guía-de-uso-paso-a-paso)
12. [Privacidad y almacenamiento](#12-privacidad-y-almacenamiento)
13. [Despliegue y compatibilidad](#13-despliegue-y-compatibilidad)
14. [Glosario técnico](#14-glosario-técnico)

---

## 1. Descripción general

El **Boticario Digital** es una aplicación web educativa interactiva que digitaliza el inventario académico de 101 plantas medicinales documentadas para Puerto Rico por el Prof. Ricardo Juan Morales De Jesús en el marco del curso CIFI 4996 de la Universidad de Puerto Rico (2022).

La aplicación proporciona acceso libre, interactivo y estructurado a información etnobotánica, botánica, fitoquímica y de preparación medicinal de cada planta. Está diseñada para estudiantes, profesionales de salud comunitaria, herbolarios y el público general.

### Características estadísticas del inventario

| Indicador | Valor |
|---|---|
| Plantas documentadas | 101 |
| Familias botánicas | 48 |
| Indicaciones medicinales totales | 436 |
| Preparaciones documentadas | 202 |
| Plantas MVP (alta completitud) | 15 |
| Plantas con fotografía CC | 15 |
| Plantas de alto riesgo | 8 |
| Términos en glosario | 40 |
| Sistemas corporales cubiertos | 11 |
| Completitud promedio MVP | 97% |
| Completitud promedio inventario completo | 69% |

### Plantas MVP (15 plantas estrella)

Anamú · Canela · Cariaquito · Culantro del monte · Cundeamor · Guanábana · Guayabo · Jengibre dulce · Limoncillo · Malagueta · Manzanilla · Parcha · Romero · Sábila · Yerba buena

---

## 2. Fundamento conceptual

### 2.1 El patrimonio herbolario de Puerto Rico

La herbolaria puertorriqueña es el resultado de la fusión histórica de tres tradiciones médicas:

**Medicina taína:** Los taínos, pueblo originario de Puerto Rico, desarrollaron un sistema médico sofisticado centrado en plantas nativas. El behíque (médico-chamán) custodiaba ese conocimiento. Plantas como el guayabo, la parcha, el anamú y la malagueta tienen raíces profundas en esta tradición. Muchos nombres vernaculares son de origen taíno.

**Medicina africana:** Las personas de origen africano traídas durante la colonización aportaron conocimiento herbolario de tradiciones de África occidental. Plantas como el anamú, la malagueta y diversas hierbas del solar tienen conexión directa con estas tradiciones. Este conocimiento pervive en botánicas, curanderos y transmisión oral familiar.

**Medicina española y europea:** La colonización española introdujo plantas mediterráneas que hoy son parte esencial de la herbolaria puertorriqueña: manzanilla, romero, ruda, canela, toronjil, mejorana, llantén. La fusión de los tres sistemas creó una herbolaria única en el Caribe.

### 2.2 Justificación de la digitalización

El inventario CIFI 4996 existe únicamente en formato académico impreso, lo que limita su accesibilidad. La digitalización responde a tres necesidades:

1. **Preservación:** Documentar el conocimiento en formato perdurable y replicable antes de que se pierda por discontinuidad generacional
2. **Acceso:** Hacer el inventario disponible para cualquier persona con un navegador web, sin barreras económicas ni geográficas
3. **Seguridad:** Incluir información de riesgo, contraindicaciones e interacciones para un uso responsable

### 2.3 Principios de diseño del proyecto

- **Educativo, no prescriptivo:** Toda información es referencial. El sistema incluye avisos médicos en múltiples niveles
- **Culturalmente respetuoso:** Se reconocen los custodios del conocimiento por tradición (taína, africana, española, académica)
- **Científicamente fundamentado:** Las indicaciones incluyen nivel de evidencia (revisión sistemática, ensayo clínico, animal, in vitro, tradicional)
- **Progresivamente enriquecible:** Diseño de datos que permite completar campos vacíos sin romper la estructura existente

---

## 3. Arquitectura técnica

### 3.1 Paradigma de la aplicación

El Boticario Digital es una **Single-Page Application (SPA) standalone** implementada sin frameworks ni dependencias de servidor de aplicaciones. La arquitectura es:

```
┌─────────────────────────────────────────────────┐
│                   index.html                    │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐  │
│  │  CSS3    │  │   HTML5  │  │ JavaScript   │  │
│  │ (estilos)│  │ (layout) │  │ (lógica SPA) │  │
│  └──────────┘  └──────────┘  └──────┬───────┘  │
└─────────────────────────────────────│───────────┘
                                      │ fetch()
                              ┌───────▼────────┐
                              │  plantas.json  │
                              │ (101 plantas)  │
                              └────────────────┘
```

### 3.2 Flujo de inicialización

```
Carga del navegador
       ↓
Parseo de HTML/CSS → DOM construido
       ↓
Ejecución de JavaScript → loadData()
       ↓
fetch('plantas.json') → Parse JSON → PLANTAS[]
       ↓
render() → renderiza catálogo inicial
       ↓
goPage('cat', btn) → muestra página de catálogo
       ↓
Usuario interactúa → event handlers → re-render
```

### 3.3 Modelo de estado de la aplicación

El estado de la interfaz se mantiene en variables globales JavaScript:

| Variable | Tipo | Valor inicial | Propósito |
|---|---|---|---|
| `PLANTAS` | Array | `[]` | Dataset completo cargado desde JSON |
| `uso` | String | `'todas'` | Filtro por sistema corporal activo |
| `risk` | String\|null | `null` | Filtro de nivel de riesgo activo |
| `tipo` | String\|null | `null` | Filtro por tipo de planta activo |
| `mvpOnly` | Boolean | `false` | Filtro de plantas MVP |
| `q` | String | `''` | Texto de búsqueda activo |
| `view` | String | `'grid'` | Vista del catálogo (grid/list) |
| `sort` | String | `'az'` | Criterio de ordenación |
| `prepT` | String | `'todas'` | Filtro de tipo de preparación |
| `glosCat` | String | `'todos'` | Categoría de glosario activa |
| `curPage` | String | `'cat'` | Página activa de la SPA |

### 3.4 Dependencias externas

| Dependencia | URL | Propósito |
|---|---|---|
| Google Fonts | fonts.googleapis.com | Tipografías (Crimson Pro, Lora, IBM Plex Mono) |
| Wikimedia Commons | upload.wikimedia.org | Fotografías de plantas (CC BY-SA) |

La aplicación no tiene dependencias de JavaScript externas (sin jQuery, React, Vue, etc.).

---

## 4. Estructura de archivos

```
boticario-digital/
│
├── index.html                              # Aplicación web principal
│   ├── <head> — metadatos, CSS, fuentes
│   ├── <body> — estructura HTML de la SPA
│   └── <script> — lógica completa de la aplicación
│
├── plantas.json                            # Base de datos operativa
│   └── Array de 101 objetos planta con 25 campos cada uno
│
├── boticario_101_plantas_completo.json     # Fuente canónica de datos
│   └── Versión completa para desarrollo y enriquecimiento
│
├── Boticario_Digital_MVP_HTML_Full.html    # Versión anterior standalone
│   └── Datos de las 15 plantas MVP embebidos directamente en JS
│
├── README.md                               # Guía de inicio rápido
├── DOCUMENTACION.md                        # Este archivo
├── DOCUMENTACION.pdf                       # Versión PDF de esta documentación
└── CIERRE_DE_SESION.md                     # Acta formal de sesión
```

### 4.1 Relación entre archivos de datos

`plantas.json` es el archivo operativo que consume `index.html`. Es un subset del `boticario_101_plantas_completo.json` que sirve como fuente canónica para desarrollo. Ambos tienen el mismo schema; la diferencia es el grado de enriquecimiento de algunos campos.

---

## 5. Funcionalidades y algoritmos

### 5.1 Sistema de navegación de páginas

La aplicación implementa una SPA con cuatro páginas: Catálogo, Preparaciones, Glosario y Aprendizaje.

**Algoritmo de cambio de página (`goPage`):**
```
1. Actualizar variable curPage
2. Remover clase 'on' de todos los elementos .page
3. Remover clase 'on' de todos los .ntab
4. Agregar clase 'on' al elemento #<página>-page
5. Agregar clase 'on' al botón de navegación
6. Mostrar/ocultar barra de búsqueda y filtros (solo en cat)
7. Si página = preps → llamar renderPreps()
8. Si página = glos → llamar renderGlos()
9. Si página = apr → llamar renderApr()
```

### 5.2 Motor de búsqueda y filtrado del catálogo

**Función `filtered()` — Pipeline de filtrado:**

```
PLANTAS[]
   │
   ├─ Filtro MVP: si mvpOnly=true, excluir plantas no en MVP_IDS
   │
   ├─ Filtro de búsqueda (q):
   │   ├─ Normalizar q con norm() (quitar acentos, minúsculas)
   │   ├─ Construir haystack: nombre + nombre científico + familia
   │   │   + indicaciones + nombres alternativos
   │   └─ Incluir si haystack.includes(qNormalizado)
   │
   ├─ Filtro por sistema corporal (uso):
   │   └─ Incluir si alguna indicación tiene .s === uso
   │
   ├─ Filtro por riesgo (risk):
   │   └─ Incluir si planta.risk === risk
   │
   ├─ Filtro por tipo (tipo):
   │   └─ Incluir si planta.tipo === tipo
   │
   └─ Ordenación según sort:
       ├─ 'az': localeCompare de nombre normalizado (ascendente)
       ├─ 'za': localeCompare de nombre normalizado (descendente)
       ├─ 'riesgo': por índice {alto:0, moderado:1, bajo:2}
       ├─ 'usos': por cantidad de indicaciones (descendente)
       └─ 'completitud': por campo completitud (descendente)
```

**Función `norm(s)` — Normalización de texto:**
```javascript
s.normalize('NFD').replace(/[̀-ͯ]/g, '').toLowerCase()
```
Descompone caracteres Unicode en forma canónica (NFD), elimina diacríticos (código U+0300–U+036F) y convierte a minúsculas. Esto permite búsquedas insensibles a acentos.

### 5.3 Renderizado del catálogo — Vista Grid y Lista

**Vista Grid (`buildCard` cuando `view='grid'`):**
- Muestra foto de miniatura (120px altura) si está disponible
- Barra de color de riesgo (3px) en la parte superior
- Nombre, nombre científico, tres primeras indicaciones
- Tags: tipo de planta, advertencia (si aplica), MVP (si aplica), foto disponible

**Vista Lista (`buildCard` cuando `view='list'`):**
- Ocupa el ancho completo del contenedor
- Grid de 3 columnas: nombre+científico | tags de indicaciones | flecha
- Borde izquierdo de color según nivel de riesgo
- Oculta: foto, familia, descripción, tags de pie de tarjeta

**Optimización de imágenes:**
- Fotos se cargan con `loading="lazy"` (lazy loading nativo del navegador)
- Manejo de error `onerror`: si la imagen falla, se elimina del DOM y se muestra la barra de color en su lugar

### 5.4 Modal de ficha de planta

El modal se abre con `openM(id)` y presenta 4 pestañas de información:

**Pestaña 0 — Tradición cultural:**
- Nombres en diferentes idiomas/tradiciones (español PR, taíno, inglés, africano, otro)
- Historia y narrativa cultural específica
- Sistemas médicos asociados (medicina taína, africana, española colonial, china, ayurvédica, caribeña, latinoamericana)
- Custodios del conocimiento: nombre, rol, nota narrativa
- Origen geográfico
- Barra de progreso de completitud del campo de datos

**Pestaña 1 — Botánica:**
- Familia botánica y tipo de planta
- Descripción morfológica
- Claves de identificación visual (lista con puntos verdes)
- Partes de la planta utilizadas en medicina

**Pestaña 2 — Fitoquímica:**
- Compuestos bioactivos: nombre (tipografía monoespaciada), clase química, mecanismo de acción
- Indicaciones medicinales con nivel de evidencia (código de color por categoría)

**Pestaña 3 — Uso Práctico:**
- Advertencias generales (si aplica)
- Preparaciones: nombre, indicación, pasos numerados, dosis/frecuencia/duración, notas
- Contraindicaciones: absolutas (✕), relativas (!), precauciones (~)
- Interacciones medicamentosas: graves (fondo rojo) y moderadas (fondo ámbar)
- Dosis máxima
- Referencias bibliográficas

### 5.5 Módulo de Preparaciones

Lista todas las preparaciones del inventario, agrupadas y filtradas por tipo (infusión, decocción, cataplasma, etc.).

**Algoritmo `renderPreps()`:**
```
1. Iterar sobre todas las plantas
2. Para cada planta, iterar sobre sus preparaciones
3. Si prepT='todas' O pr.tipo === prepT: incluir
4. Renderizar cada preparación como tarjeta colapsable
5. togglePrep(i): alterna clase 'open' en el cuerpo de la tarjeta
```

**Tipos de preparaciones y conteo:**

| Tipo | Cantidad |
|---|---|
| Infusión | 106 |
| Decocción | 25 |
| Cataplasma | 17 |
| Jugo | 20 |
| Aceite | 13 |
| Gel/Crema | 6 |
| Baño | 7 |
| Tintura | 4 |
| Vaporización | 4 |
| **Total** | **202** |

### 5.6 Glosario botánico y fitoquímico

40 términos clasificados en 9 categorías:

| Categoría | Ejemplos de términos |
|---|---|
| Fitoquímica | Acemannan, Alicina, Flavonoide, Gingerol, Mentol |
| Acción farmacológica | Astringente, Carminativo, Demulcente, Diurético |
| Preparaciones | Infusión, Decocción, Tintura, Macerar |
| Seguridad | Contraindicación, Interacción medicamentosa, Uterotónico |
| Botánica | Rizoma |
| Cultura | Custodio del conocimiento |
| Sistema médico | Medicina taína, Ayurveda |
| Evidencia | Evidencia in vitro, Revisión sistemática, Nivel de evidencia |
| Ciencia | Etnobotánica |

**Algoritmo `renderGlos()`:**
```
1. Filtrar GLOSARIO por glosCat (o mostrar todos)
2. Ordenar alfabéticamente en español (localeCompare con 'es')
3. Renderizar botones de categoría + lista de términos
```

### 5.7 Página de Aprendizaje y Contexto Cultural

Genera dinámicamente estadísticas del inventario cargado y presenta:
- Estadísticas: total plantas, MVP, indicaciones, con fitoquímica completa, sistemas, familias
- Sistema de seguridad: descripción de los 3 niveles de riesgo con conteo actual
- Los tres pilares culturales: taíno, africano, español
- Información sobre la fuente CIFI 4996

---

## 6. Esquema de datos

### 6.1 Estructura del objeto planta

Cada planta en `plantas.json` sigue este schema JSON:

```json
{
  "id": "string",
  "n": "string",
  "sci": "string",
  "fam": "string",
  "tipo": "enum[hierba|árbol|arbusto|trepadora|suculenta|gramínea]",
  "origen": "string",
  "hist": "string",
  "nombres": [
    {
      "i": "enum[español_pr|taino|ingles|africano|otro]",
      "n": "string"
    }
  ],
  "sistemas": ["enum[medicina_taína|medicina_africana|medicina_española_colonial|medicina_china|ayurveda|medicina_caribeña|medicina_latinoamericana]"],
  "custodios": [
    {
      "nom": "string",
      "rol": "enum[custodio_indigena|custodio_historico|custodio_comunitario|custodio_academico]",
      "nota": "string"
    }
  ],
  "partes": ["string"],
  "habitats": ["string"],
  "morfo": "string",
  "claves": ["string"],
  "foto": {
    "thumb": "string (URL)",
    "full": "string (URL)",
    "attr": "string (crédito CC)"
  },
  "ind": [
    {
      "c": "string (condición/indicación)",
      "s": "enum[digestivo|nervioso|respiratorio|musculoesqueletico|metabolico|cardiovascular|dermatologico|inmune|reproductivo|urinario|general]",
      "e": "enum[revision_sistematica|ensayo_clinico|animal|in_vitro|tradicional]"
    }
  ],
  "comp": [
    {
      "n": "string (nombre compuesto)",
      "cl": "string (clase química)",
      "m": "string (mecanismo de acción)"
    }
  ],
  "preps": [
    {
      "nom": "string",
      "tipo": "enum[infusion|decoccion|tintura|aceite|jugo|bano|crema|cataplasma|capsula|vaporizacion]",
      "ind": "string",
      "pasos": [
        {"o": "number", "i": "string"}
      ],
      "dosis": {
        "c": "string (cantidad)",
        "f": "string (frecuencia)",
        "d": "string (duración)"
      },
      "notas": "string"
    }
  ],
  "risk": "enum[alto|moderado|bajo]",
  "adv": "string | null",
  "contraind": [
    {
      "s": "enum[absoluta|relativa|precaucion]",
      "d": "string"
    }
  ],
  "interacc": [
    {
      "med": "string",
      "ef": "string",
      "s": "enum[grave|moderada|leve]"
    }
  ],
  "dmax": "string | null",
  "completitud": "number (0-100)",
  "refs": ["string"]
}
```

### 6.2 Descripción de campos

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | String | Identificador único en kebab-case (ej: `"yerba-buena"`) |
| `n` | String | Nombre vernacular principal en español de Puerto Rico |
| `sci` | String | Nombre científico (binomial en cursiva por convención) |
| `fam` | String | Familia botánica |
| `tipo` | Enum | Categoría morfológica de la planta |
| `origen` | String | Origen geográfico/región nativa |
| `hist` | String | Narrativa histórica y cultural de la planta |
| `nombres` | Array | Nombres en diferentes idiomas y tradiciones |
| `sistemas` | Array | Sistemas médicos tradicionales que la usan |
| `custodios` | Array | Personas/grupos custodios del conocimiento |
| `partes` | Array | Partes de la planta con uso medicinal |
| `habitats` | Array | Ambientes donde crece naturalmente |
| `morfo` | String | Descripción morfológica para identificación |
| `claves` | Array | Características visuales clave para identificar |
| `foto` | Object | URLs de foto y crédito de autor (CC) |
| `ind` | Array | Indicaciones médicas con sistema y nivel de evidencia |
| `comp` | Array | Compuestos bioactivos con clase y mecanismo |
| `preps` | Array | Preparaciones medicinales paso a paso |
| `risk` | Enum | Nivel de riesgo de seguridad (alto/moderado/bajo) |
| `adv` | String | Advertencia de seguridad prominente (o null) |
| `contraind` | Array | Contraindicaciones absolutas, relativas y precauciones |
| `interacc` | Array | Interacciones con medicamentos convencionales |
| `dmax` | String | Dosis máxima documentada (o null) |
| `completitud` | Number | Porcentaje de campos completos (0-100) |
| `refs` | Array | Referencias bibliográficas en formato texto |

### 6.3 Enums y valores válidos

**Nivel de riesgo (`risk`):**
- `"alto"` — Contraindicada en embarazo o con efectos tóxicos conocidos. Requiere supervisión médica
- `"moderado"` — Requiere precaución en ciertos grupos poblacionales o dosis
- `"bajo"` — Generalmente segura a dosis normales para adultos sanos

**Nivel de evidencia (`ind[].e`):**

| Código | Descripción | Color UI |
|---|---|---|
| `revision_sistematica` | Síntesis de múltiples estudios | Verde (#EAF3DE) |
| `ensayo_clinico` | Estudio controlado en humanos | Azul (#E6F1FB) |
| `animal` | Estudios en modelos animales | Ámbar (#FAEEDA) |
| `in_vitro` | Estudios en células/laboratorio | Morado (#F5F0FA) |
| `tradicional` | Uso tradicional documentado | Gris (--bd) |

**Sistema corporal (`ind[].s`):**

| Código | Sistemas |
|---|---|
| `digestivo` | Sistema digestivo |
| `nervioso` | Sistema nervioso |
| `respiratorio` | Sistema respiratorio |
| `musculoesqueletico` | Músculo-esquelético |
| `metabolico` | Metabólico/endocrino |
| `cardiovascular` | Cardiovascular |
| `dermatologico` | Dermatológico |
| `inmune` | Sistema inmune |
| `reproductivo` | Sistema reproductivo |
| `urinario` | Sistema urinario |
| `general` | General/sistémico |

---

## 7. Funciones y métodos documentados

### 7.1 Carga de datos

```javascript
async function loadData()
```
**Propósito:** Carga asíncronamente `plantas.json` y inicializa la aplicación.  
**Flujo:** fetch() → JSON.parse → asignar a `PLANTAS` → `render()` → `renderPreps()`  
**Error handling:** Si el fetch falla, muestra mensaje de error en el grid con instrucciones de uso correcto

### 7.2 Navegación

```javascript
function goPage(p, btn)
```
**Parámetros:** `p` — id de la página ('cat'|'preps'|'glos'|'apr') · `btn` — elemento DOM del botón de navegación  
**Efectos:** Muestra la página seleccionada, oculta las demás, activa el tab correspondiente, controla visibilidad de barra de búsqueda/filtros

### 7.3 Filtrado y renderizado del catálogo

```javascript
function filtered() → Array
```
**Retorna:** Array de plantas que pasan todos los filtros activos, ordenadas según `sort`  
**Complejidad:** O(n × m) donde n=total plantas, m=cantidad de indicaciones por planta (para filtro por uso)

```javascript
function render()
```
**Propósito:** Renderiza el catálogo completo según el estado de filtros  
**Efectos:** Actualiza contador de resultados · llama `filtered()` · genera HTML con `buildCard()` · asigna al DOM

```javascript
function buildCard(p) → String
```
**Parámetros:** `p` — objeto planta  
**Retorna:** String HTML de la tarjeta (diferente según `view`)

### 7.4 Interacciones de filtros

```javascript
function onSearch(v)
function clearSi()
function setUso(v, btn)
function togR(v, btn)
function togT(v, btn)
function togMVP(btn)
function setV(v)
```

Cada función actualiza la variable de estado correspondiente y llama `render()`. Los filtros `togR` y `togT` implementan un toggle — si el mismo valor ya está activo, lo desactiva (regresa a null).

### 7.5 Modal de ficha

```javascript
function openM(id)
```
**Parámetros:** `id` — id único de la planta  
**Propósito:** Busca la planta en `PLANTAS`, construye el HTML de las 4 pestañas del modal, muestra el overlay  
**Efectos secundarios:** Abre `#moverlay` con clase 'open' · resetea scroll del body del modal a 0 · activa pestaña 0

```javascript
function closeM(event)
function closeMD()
```
`closeM` cierra el modal solo si el clic fue sobre el overlay (no sobre el modal en sí).  
`closeMD` cierra el modal incondicionalmente.

```javascript
function mTab(i)
```
**Parámetros:** `i` — índice de pestaña (0-3)  
**Efectos:** Activa el tab `mt{i}` y el contenido `mc{i}`, desactiva los demás

### 7.6 Preparaciones

```javascript
function renderPreps()
```
Recorre `PLANTAS` y construye la lista de preparaciones filtradas por `prepT`. Cada tarjeta es colapsable.

```javascript
function togglePrep(i)
```
Alterna la clase `'open'` en el elemento `#pb{i}`, expandiendo/colapsando el cuerpo de la preparación.

```javascript
function setPrepT(v, btn)
```
Actualiza `prepT` y llama `renderPreps()`.

### 7.7 Glosario

```javascript
function renderGlos()
```
Filtra `GLOSARIO` por `glosCat`, ordena alfabéticamente en español y renderiza con botones de categoría.

```javascript
function setGlosCat(v, btn)
```
Actualiza `glosCat` y llama `renderGlos()`.

### 7.8 Aprendizaje

```javascript
function renderApr()
```
Calcula estadísticas dinámicas del inventario cargado y renderiza la página de aprendizaje con cuatro secciones: estadísticas, sistema de seguridad, pilares culturales, fuente CIFI 4996.

---

## 8. Sistema de diseño

### 8.1 Paleta de colores

La paleta está definida en CSS Custom Properties en `:root`:

| Variable | Valor | Uso |
|---|---|---|
| `--v` | `#2D5016` | Verde primario — color de marca |
| `--vl` | `#3a6b1c` | Verde claro — hover, accents |
| `--vd` | `#1e3a0e` | Verde oscuro — footer, énfasis |
| `--vp` | `#EAF3DE` | Verde pálido — fondos informativos |
| `--vpm` | `#C0DD97` | Verde medio — bordes verdes, separadores |
| `--ocre` | `#C67F3E` | Ocre — tabs activos, acentos cálidos |
| `--azul` | `#3B5A7D` | Azul — nombres científicos, compuestos |
| `--morado` | `#6B4E71` | Morado — sistemas médicos |
| `--rojo` | `#9B2335` | Rojo — advertencias, riesgo alto |
| `--rp` | `#FFF0F1` | Rojo pálido — fondos de advertencia |
| `--amb` | `#B47A2E` | Ámbar — riesgo moderado |
| `--ap` | `#FFF8EE` | Ámbar pálido — fondos de moderado |
| `--beige` | `#F5F1E8` | Beige — fondo principal |
| `--paper` | `#FAF7F0` | Paper — fondo de tarjetas |
| `--ink` | `#2B2B2B` | Tinta — texto principal |
| `--inks` | `#4a4a42` | Tinta suave — texto secundario |
| `--inkm` | `#7a7a6e` | Tinta media — texto terciario, etiquetas |

### 8.2 Tipografía

| Variable | Fuente | Uso |
|---|---|---|
| `--fd` | Crimson Pro, Georgia, serif | Títulos, nombres de plantas, tabs de modal |
| `--fb` | Lora, Georgia, serif | Cuerpo de texto, botones |
| `--fm` | IBM Plex Mono, monospace | Nombres de compuestos, badges técnicos |

**Escala tipográfica:** Base 16px con escala fluida. Tamaños desde 9px (etiquetas pequeñas) hasta 2rem (números estadísticos).

### 8.3 Espaciado y formas

- **Radio de borde principal** (`--r`): 10px — tarjetas, modal
- **Radio de borde menor** (`--rm`): 7px — elementos internos
- **Radio de borde mínimo**: 4-6px — badges, pills

### 8.4 Sistema de barras de color de riesgo

Cada planta muestra una barra visual de 3px en la parte superior de la tarjeta o un borde izquierdo de 3px en vista lista, codificado por riesgo:

- 🔴 `--rojo` (#9B2335) — Alto riesgo
- 🟡 `--amb` (#B47A2E) — Riesgo moderado
- 🟢 `--v` (#2D5016) — Bajo riesgo

### 8.5 Jerarquía visual de pestañas

Las pestañas activas se señalan con:
- **Header:** borde inferior ámbar (`--ocre`) de 2.5px en tabs de navegación principal
- **Modal:** borde inferior verde (`--v`) de 2px + fondo `--paper` en tabs del modal
- **Filtros:** background del color temático + texto blanco en filtros activos

---

## 9. Accesibilidad

### 9.1 Implementaciones actuales

- **Role dialog:** El modal tiene `role="dialog"` y `aria-modal="true"`
- **Keyboard navigation:** Tecla `Escape` cierra el modal (listener en `document`)
- **Placeholder descriptivo:** Input de búsqueda tiene placeholder explicativo
- **Alt text:** Imágenes de plantas tienen `alt` con el nombre vernacular
- **Aviso médico:** Disclaimer visible en la parte superior con opción de cierre
- **Semántica HTML:** Uso de `<header>`, `<nav>`, `<footer>`, `<button>`, `<select>`

### 9.2 Áreas de mejora futura

- Agregar `aria-label` a botones de filtro
- Implementar `aria-expanded` en tarjetas colapsables de preparaciones
- Agregar `aria-live` para anunciar cambios en el contador de resultados
- Aumentar contraste en texto `--inkm` para cumplir WCAG AA (4.5:1)
- Agregar `focus-visible` consistente para navegación por teclado

---

## 10. Diseño responsivo

La aplicación implementa diseño mobile-first con tres breakpoints:

### 10.1 Breakpoints

| Breakpoint | Ancho | Ajustes |
|---|---|---|
| Mobile S | ≤ 340px | Grid de 1 columna |
| Mobile | ≤ 420px | Grid de 2 columnas, padding reducido, foto 90px, ocultar subtítulos en modal |
| Tablet+ | ≥ 640px | Grid auto-fill con mínimo 210px por columna |
| Desktop | ≥ 900px | Grid auto-fill con mínimo 220px, gap 10px |

### 10.2 Comportamiento responsivo del header

El header es sticky (`position: sticky; top: 0`). En móvil, los tabs de navegación y filtros son horizontalmente scrollables (`overflow-x: auto; scrollbar-width: none`) con `-webkit-overflow-scrolling: touch` para inercia en iOS.

### 10.3 Vista lista vs. grid

| Elemento | Vista Grid | Vista Lista |
|---|---|---|
| Layout | `repeat(auto-fill, minmax(195px, 1fr))` | `1fr` (columna única) |
| Foto | Visible (120px) | Oculta |
| Familia | Visible | Oculta |
| Indicaciones | 2 líneas truncadas | Ocultas |
| Tags de pie | Visibles | Ocultos |
| Identificación de riesgo | Barra superior | Borde izquierdo 3px |

### 10.4 Modal responsivo

En móvil (≤ 420px):
- Foto reducida a 140px altura
- Nombre de planta reducido a 1.35rem
- Subtítulos de pestañas ocultos (clase `mtsub`)
- Dosis cambia a columna única

El modal siempre ocupa `max-width: 660px` y se centra en pantalla, con `max-height: 55vh` para el cuerpo y scroll interno.

---

## 11. Guía de uso paso a paso

### 11.1 Explorar el catálogo

1. Al abrir la aplicación, el catálogo muestra las 101 plantas en orden alfabético
2. Usar la barra de búsqueda para filtrar por nombre, uso o familia botánica
3. Usar los tabs horizontales (Digestión, Nervios, Respiratorio...) para filtrar por sistema corporal
4. Usar los filtros de la segunda fila para filtrar por nivel de riesgo, tipo de planta o solo MVP
5. Usar el selector de ordenación para cambiar el criterio (A→Z, Z→A, Mayor riesgo, Más usos, Más completas)
6. Alternar entre vista cuadrícula (⊞) y vista lista (☰) con los botones de la derecha

### 11.2 Ver la ficha de una planta

1. Hacer clic en cualquier tarjeta del catálogo para abrir el modal
2. La pestaña **Tradición** muestra la historia cultural, nombres, sistemas médicos y custodios
3. La pestaña **Botánica** muestra morfología, claves de identificación y partes utilizadas
4. La pestaña **Fitoquímica** muestra compuestos bioactivos con su mecanismo y las indicaciones con nivel de evidencia
5. La pestaña **Uso Práctico** muestra preparaciones paso a paso, contraindicaciones e interacciones
6. Cerrar el modal haciendo clic en × o fuera del modal, o presionando Escape

### 11.3 Explorar preparaciones

1. Ir a la pestaña **⚗️ Preparaciones** en la navegación superior
2. Usar los filtros de tipo (Infusión, Decocción, Cataplasma...) para filtrar
3. Hacer clic en cualquier preparación para expandirla y ver los pasos detallados
4. Cada preparación muestra: planta, nombre de la preparación, indicación, pasos numerados, dosis, frecuencia y duración

### 11.4 Consultar el glosario

1. Ir a la pestaña **📖 Glosario** en la navegación superior
2. Usar los filtros de categoría para ver términos de fitoquímica, preparaciones, seguridad, etc.
3. Los términos están ordenados alfabéticamente en español

### 11.5 Aprender sobre el contexto

1. Ir a la pestaña **🌱 Aprendizaje** en la navegación superior
2. Ver las estadísticas actuales del inventario cargado
3. Revisar el sistema de seguridad y los tres pilares culturales

---

## 12. Privacidad y almacenamiento

### 12.1 Datos del usuario

El Boticario Digital **no recopila, almacena ni transmite datos del usuario**. No hay:
- Cuentas de usuario ni autenticación
- Cookies de seguimiento o analíticas
- Formularios que envíen datos a un servidor
- LocalStorage o SessionStorage utilizados
- Scripts de terceros de analítica (Google Analytics, etc.)

### 12.2 Solicitudes de red que realiza la aplicación

Al cargar, la aplicación hace las siguientes solicitudes externas:

| Solicitud | Destinatario | Propósito |
|---|---|---|
| CSS de fuentes | fonts.googleapis.com | Cargar familia de fuentes (Crimson Pro, Lora, IBM Plex Mono) |
| Archivos de fuentes | fonts.gstatic.com | Descargar archivos .woff2 de fuentes |
| Fotos de plantas | upload.wikimedia.org | Imágenes de las 15 plantas MVP (CC BY-SA) |
| `plantas.json` | Mismo servidor | Base de datos de plantas |

### 12.3 Modo offline

La aplicación no funciona completamente offline de fábrica (requiere `plantas.json` y fuentes remotas). Para uso offline completo:
- Descargar y referenciar fuentes localmente
- Descargar fotos de Wikimedia y actualizar URLs en el JSON
- La aplicación en sí (HTML + JSON locales) puede servirse desde cualquier servidor o filesystem con servidor web

---

## 13. Despliegue y compatibilidad

### 13.1 Requisitos de despliegue

La aplicación requiere únicamente un servidor HTTP capaz de servir archivos estáticos. No requiere:
- Base de datos
- Lenguaje de servidor (PHP, Node, Python, etc.)
- Autenticación
- Variables de entorno

**Mínimo viable:** Cualquier servidor capaz de servir `index.html` y `plantas.json` con el header correcto de Content-Type.

### 13.2 Opciones de despliegue

| Plataforma | Configuración | Costo |
|---|---|---|
| GitHub Pages | Repositorio público → Settings → Pages → rama main | Gratuito |
| Netlify | Conectar repositorio GitHub → rama main | Gratuito (plan Starter) |
| Vercel | Conectar repositorio → sin configuración adicional | Gratuito (plan Hobby) |
| Cloudflare Pages | Conectar repositorio → build command vacío | Gratuito |
| nginx (propio) | `root /path/to/repo;` | Costo de servidor |
| Apache (propio) | `DocumentRoot /path/to/repo` | Costo de servidor |

### 13.3 Despliegue actual

La aplicación está desplegada en **GitHub Pages** en:  
`https://ricardojuanmorales.github.io/boticario-digital/`

### 13.4 Compatibilidad de navegadores

| Característica CSS/JS | Requerida por | Soporte mínimo |
|---|---|---|
| CSS Custom Properties | Todo el sistema de diseño | Chrome 49 / Firefox 31 / Safari 9.1 |
| CSS Grid | Layout de catálogo | Chrome 57 / Firefox 52 / Safari 10.1 |
| `fetch()` API | Carga de datos | Chrome 42 / Firefox 39 / Safari 10.1 |
| `async/await` | `loadData()` | Chrome 55 / Firefox 52 / Safari 10.1 |
| `loading="lazy"` | Lazy load de imágenes | Chrome 77 / Firefox 75 / Safari 15.4 |
| `backdrop-filter` | Blur del overlay modal | Chrome 76 / Firefox 103 / Safari 9 |
| Unicode NFD (norm) | Motor de búsqueda | Todos los navegadores modernos |

**Recomendación:** Chrome 88+, Firefox 85+, Safari 14+ para experiencia completa.

### 13.5 Consideraciones de rendimiento

- **Tamaño de `plantas.json`:** ~449 KB. Se descarga una sola vez y se mantiene en memoria
- **Imágenes:** Carga lazy nativa; solo las 15 MVP tienen foto remota
- **JavaScript:** Vanilla JS sin dependencias; parse y renderizado completo en < 50ms en hardware moderno
- **CSS:** Todo inline en el HTML; sin solicitudes adicionales de CSS externo

---

## 14. Glosario técnico

| Término | Definición |
|---|---|
| **SPA** | Single-Page Application — aplicación donde toda la lógica de navegación ocurre en el cliente sin recargar la página |
| **Vanilla JS** | JavaScript puro sin frameworks ni librerías externas |
| **CSS Custom Properties** | Variables nativas de CSS definidas con la sintaxis `--nombre: valor` |
| **fetch API** | API web nativa para realizar solicitudes HTTP asíncronas desde JavaScript |
| **Lazy loading** | Técnica de carga diferida de imágenes hasta que son visibles en el viewport |
| **kebab-case** | Convención de nomenclatura que usa guiones bajos (`mi-nombre-de-variable`) |
| **NFD** | Forma de normalización Unicode D — descompone caracteres acentuados en carácter base + diacrítico |
| **MVP (plantas)** | Las 15 plantas con mayor nivel de documentación y completitud en el inventario |
| **completitud** | Porcentaje de campos del schema que están completados para una planta dada |
| **CIFI 4996** | Código del curso universitario cuyo inventario académico es la fuente de datos primaria |
| **ESGE 4995** | Código del curso universitario responsable de la implementación digital |
| **CC BY-SA** | Creative Commons Attribution-ShareAlike — licencia de contenido abierto |
| **Wikimedia Commons** | Repositorio libre de imágenes y medios bajo licencias abiertas |

---

*Documentación generada el 12 de mayo de 2026*  
*Boticario Digital v2.0 · Universidad de Puerto Rico*
