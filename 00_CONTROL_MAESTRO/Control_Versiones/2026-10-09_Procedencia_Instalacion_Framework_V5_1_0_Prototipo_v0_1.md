# Procedencia · Instalación prototipo del Framework V5.1.0 en Boticario Digital 101

**Fecha:** 2026-10-09
**Estado:** PROTOTIPO · rama `prototipo/framework-v5.1.0` · no fusionado a `main`
**Modo Framework:** INTEGRATE (proyecto existente)
**Decisiones que lo originan:** D-A14 (Framework embebido en cada repositorio) y D-A15 (la app del Framework como fuente de trabajo)
**Decisión de ubicación:** Ricardo eligió instalar mezclado en la raíz (00–21 + 99 junto a los archivos del MVP), desde su clon local existente.

## Origen
| Campo | Valor |
|---|---|
| Release | Framework Genérico V5.1.0 · "estabilización arquitectónica, pedagógica y de distribución" |
| Fecha del release | 2026-10-06 |
| Archivo | `framework-generico-v5.1.0_bf708644ee11.zip` |
| SHA-256 | `96e09accaa46b4393e0dbb866b810509531eb1fab82668143f320f2e18be3193` |
| Archivos | 718 |
| Repositorio maestro | https://github.com/ricardojuanmorales/framework-proyecto-generico-ia-1 |
| Base del Boticario | commit `adbb520` (MVP, igual a `origin/main` al instalar) |

## Regla de instalación: nada del Boticario se sobrescribe
| Elemento del release | Dónde quedó | Por qué |
|---|---|---|
| Carpetas 00–21, 99, `apps/`, `legacy/`, `.release/`, `.obsidian/`, `.gitignore`, documentos raíz | Raíz, sin cambios | No chocaban con archivos del Boticario |
| `README.md` | `README_Framework_V5_1_0.md` | El `README.md` del Boticario se conserva |
| `index.html` | `index_framework_v5_1_0.html` | `index.html` es la app publicada del Boticario en GitHub Pages |
| `.github/workflows/*.yml` (5) | `10_REPOSITORIOS_Y_FLUJO_TECNICO/CI_CD/Workflows_Framework_V5_1_0_Inactivos/` | Activos en la raíz, al fusionarse con `main` reemplazarían el sitio publicado del Boticario y crearían un release "v5.1.0" ajeno a este proyecto |

## Verificación
- La huella SHA-256 del zip coincide con el archivo subido por Ricardo.
- Los 718 archivos instalados son idénticos byte a byte al release, comparados uno a uno.
- Total en el repositorio sin `.git`: 729 = 718 del Framework + 11 del MVP.

## Actualización posterior al release (2026-10-09)
Por decisión de Ricardo se incorporaron los documentos de fundamento añadidos al maestro después del release, tomados del commit `62eb6c8` del repositorio maestro:

| Archivo | Tipo |
|---|---|
| `02_ARQUITECTURA_CONCEPTUAL/Arquitecturas_Referencia/2026-10-08_Arquitectura_Conceptual_Integrada_Framework_Canon_v1_0.md` | nuevo · canon de arquitectura |
| `01_FUNDAMENTO_FILOSOFICO/Marcos_Referencia/2026-10-08_Repositorio_Epistemologico_Fundacional_Framework_Canon_v1_0.md` | nuevo · canon epistemológico |
| `18_DOCUMENTACION_ACTIVA/Cierres_Reportes/Bitacoras/2026-10-06_Bitacora_Cierre_Estabilizacion_V5_1_0_Retorno_Articulo_v1_0.md` | nuevo · bitácora |
| `01_FUNDAMENTO_FILOSOFICO/README.md`, `01_FUNDAMENTO_FILOSOFICO/Marcos_Referencia/README.md`, `02_ARQUITECTURA_CONCEPTUAL/README.md`, `18_DOCUMENTACION_ACTIVA/Cierres_Reportes/Bitacoras/README.md` | índices actualizados que enlazan los nuevos documentos |
| `README_Framework_V5_1_0.md` | README del maestro en `62eb6c8` |

El resto de los archivos sigue idéntico al release v5.1.0. Con esto, la instalación equivale al estado del maestro en `62eb6c8`.

## Advertencia de identidad documental
Los cartapacios contienen documentos **del Framework maestro**: sus decisiones, su historia y sus bitácoras. Todavía no son documentos del Boticario. Antes de fusionar hay que decidir cómo se distinguen ambos (por ejemplo, con un prefijo o un registro de autoridad documental; ver deuda D-07).
