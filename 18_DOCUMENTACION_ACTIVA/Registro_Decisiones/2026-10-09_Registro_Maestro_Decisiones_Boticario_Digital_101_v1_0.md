# Registro Maestro de Decisiones — Boticario Digital 101

**Proyecto:** Boticario Digital 101 — ruta v1.0.0 bajo SDD
**Marco rector:** Framework Genérico V4.1.0 Integral Autosostenido
**Arquetipo de referencia:** AI StoryLab 1 v1.0.0
**Estado:** activo
**Nota de formato:** D-A06 queda reemplazada por D-A17 y D-A12 por D-A28. Las decisiones D-A01 a D-A29 se registraron en formato provisional. Se reescribirán en el formato canónico de §16.2 del Framework (once campos) al abrir el Bloque 4.

---

## Bloque 1 — Decisiones de apertura

### D-A01 · Repositorio de destino
**Fecha:** 2026-09-10
**Decisión:** La refactorización ocurre dentro del repositorio existente `github.com/ricardojuanmorales/boticario-digital`.
**Justificación:** preserva los 9 commits de historia, la URL de GitHub Pages ya publicada y los enlaces externos existentes.
**Consecuencias:** el MVP histórico se preserva por triple mecanismo — tag inmutable sobre `adbb520`, cartapacio `99_ARCHIVO_HISTORICO/MVP_2026_05/`, y ruta pública `/legado/` en Pages replicando el patrón `legacy-bridge` de AI StoryLab 1.

### D-A02 · Alcance de la v1.0
**Fecha:** 2026-09-10
**Decisión:** Ruta completa — catálogo auditado **más** capa de pedagogía lúdica: misiones, herbario personal y portafolio bajo decisión humana con export/import.
**Consecuencias:** requiere SPEC-OP de diseño instruccional, modelo conceptual de evidencia/portafolio y suites de prueba de ciclo creativo.

### D-A03 · Numeración de versiones
**Fecha:** 2026-09-10
**Decisión:** MVP se congela como `v0.9.0-mvp-historico`. La ruta SDD abre en `v0.4.0` y avanza hasta `v1.0.0` con los mismos nombres de fase que AI StoryLab 1.

### D-A04 · Ritmo de trabajo
**Fecha:** 2026-09-10
**Decisión:** Avance por bloques sin fecha fija. Cada bloque abre solo cuando el anterior cierra con decisión humana registrada.
**Consecuencias:** el cronograma del Bloque 3 se expresará en secuencia y criterios de cierre, no en fechas absolutas.

---

## Bloque 1.5 — Decisiones de activación (Framework §5, §6, §8)

### D-A05 · Nivel de activación
**Fecha:** 2026-09-10
**Decisión:** **N3 — Avanzado**, con ruta declarada a N4.
**Justificación:** se cumplen las siete reglas de §6.2 (perfiles transversales, Caleidoscopio, publicación, comunidad sensible, riesgos éticos y culturales, archivo y wiki, trazabilidad). Para N4 solo se cumplen 2 de 6 condiciones de §6.3.
**Consecuencias:** obliga a los nueve documentos mínimos de §14.1. Siete están ausentes hoy: brief, changelog, CHECKS, wiki, archivo ejecutado, primer de continuidad y manifest.

### D-A06 · Modo Caleidoscopio
**Fecha:** 2026-09-10
**Decisión:** **C4 base con C5 y C6 activados como modos concurrentes.**
**Reparto de gobierno:**
- C4 (tres perfiles) → arquitectura hexagonal y ciclo SDD
- C5 (pedagógico) → misiones, herbario, portafolio, evidencia del estudiante
- C6 (comunitario) → custodia, atribución comunitaria, licencia de datos, archivo vivo
**Justificación:** el Caleidoscopio es lógica integradora, no casilla excluyente. Declarar los tres evita que la custodia comunitaria entre tarde como deuda ética.

### D-A07 · Audiencia y alcance
**Fecha:** 2026-09-10
**Decisión:** La audiencia **incluye menores / K-12** y se **esperan colaboradores externos** vía PR.
**Consecuencias directas:**
- El JSON Schema de `plantas.json` deja de ser mejora y pasa a ser **contrato obligatorio con validación en CI** — sin él, un PR externo puede romper el catálogo o introducir contenido sanitario no verificado.
- Se activa gobernanza de contribución: revisión humana obligatoria de PRs que toquen datos de plantas, con atención especial a riesgo, contraindicaciones e interacciones.
- El herbario personal (D-A02) puede generar datos de menores. Privacidad por defecto pasa de principio a requisito verificable.
- **Abre R-01** (ver abajo).
**Nota:** no se confirmó adopción institucional formal por la UPR. N4 permanece como ruta, no como estado.

### D-A08 · Destinatario de la continuidad
**Fecha:** 2026-09-10
**Decisión:** El trabajo debe poder ser retomado por **un colega docente sin contexto previo**.
**Consecuencias:** el cartapacio `21_WIKI_DOCUMENTACION_HUMANA` deja de ser opcional. Exige guía docente, explicación del método en lenguaje humano y glosa de decisiones vigentes. Es también lo que hace el proyecto transferible como arquetipo a otros cursos.

---

## Bloque FICHA-1 — Ficha estandarizada (piloto: Anamú)

**Insumo:** `claude/FICHA-B1_Diagnostico_Anamu.md` · **Fecha:** 2026-10-09 · **Gates:** G5, G7, G9

### D-A09 · Dosis sin respaldo clínico
**Fecha:** 2026-10-09
**Decisión:** las dosis tradicionales se conservan, pero solo **rotuladas** como "reportada por tradición, no validada clínicamente", con su fuente y solo para la población adulta. En el modo escolar se ocultan.
**Consecuencias:** el esquema añade `dosis.estatus` (`validada_clinica` | `tradicional_reportada`) y `dosis.fuente`. La superficie escolar filtra por este campo. Es un insumo directo para cerrar **R-01**.

### D-A10 · Severidad de seguridad frente a evidencia
**Fecha:** 2026-10-09
**Decisión:** se conserva la severidad cautelosa del inventario y se añade un campo de **certeza** a cada contraindicación, interacción y efecto: `documentada` | `precautoria_por_falta_de_datos`.
**Consecuencias:** ninguna advertencia se debilita. Cada advertencia declara si se apoya en una fuente o en el principio de precaución.

### D-A11 · Imágenes generadas con IA
**Fecha:** 2026-10-09
**Decisión:** se aceptan ilustraciones generadas con IA en la galería.
**Consecuencias:** se mantiene obligatorio el rótulo "ilustración generada con [herramienta]; no sustituye la identificación botánica por ejemplar o especialista". El esquema añade `imagen.origen` (`foto` | `ilustracion_ia`) y `imagen.herramienta`. Queda pendiente decidir la licencia de esas imágenes cuando se resuelva D-08.

### D-A12 · Atribución de Guersom J. Báez Fonseca · **REEMPLAZADA por D-A28**
**Fecha:** 2026-10-09
**Decisión:** figura como **revisor/a** de la evidencia de la ficha de Anamú, en el módulo M9 (custodia y atribución).

---

## Bloque FICHA-1.5 — Aclaraciones del ecosistema (Plano del Buen Vivir)

**Insumo:** `claude/FICHA-B1.5_Plano_Conceptual_Buen_Vivir.md` · **Fecha:** 2026-10-09

### D-A13 · Local-first para todo el ecosistema
**Fecha:** 2026-10-09
**Decisión:** todas las aplicaciones del ecosistema serán local-first.
**Consecuencias:** Tablero tendrá que migrar su colaboración, que hoy depende de Google/Supabase y de un servidor. Refuerza D-A07: privacidad por defecto para audiencia K-12.

### D-A14 · Framework V5.1 embebido en cada repositorio
**Fecha:** 2026-10-09
**Decisión:** cada repositorio del ecosistema integra el Framework V5.1 dentro de sí, como lenguaje común y estructura de trabajo para una integración posterior.
**Consecuencias:** el Boticario es el primer prototipo de instalación, desde el zip del release estable v5.1.0. Las decisiones D-A05 y D-A06, tomadas con la V4.1, deben releerse con la V5.1.

### D-A15 · App del Framework como fuente de trabajo; portafolios interoperables
**Fecha:** 2026-10-09
**Decisión:** la fuente de trabajo es la app del Framework, adaptada por las personas usuarias. Cada repositorio ofrece un portafolio del tema, y los portafolios serán interoperables en una integración futura.
**Consecuencias:** el esquema `portfolio.schema.json` del Framework pasa a ser el candidato a contrato común entre repositorios. Reemplaza el "portafolio propio" previsto en D-A02 para el Boticario.

---

## Bloque FW-1/FW-2 — Prototipo e integración del Framework V5.1

**Insumos:** rama `prototipo/framework-v5.1.0` (commit `14534b9`), Ficha compacta de activación v0.1 y expediente Framework en borrador · **Fecha:** 2026-10-09

### D-A16 · Forma del Framework dentro del repositorio
**Fecha:** 2026-10-09
**Decisión:** **copia completa** del Framework V5.1.0 (release más los 3 documentos de fundamento del 8 de octubre), mezclada en la raíz, con **excepción registrada** en `04_GOBERNANZA_ETICA_Y_RIESGOS/Registro_Excepciones/2026-10-09_Excepcion_Copia_Completa_Framework_V5_1_0_Boticario_v0_1.md`.
**Justificación:** lenguaje común y estructura sólida para la integración posterior (D-A14).
**Consecuencias:**
- Exceptúa el antipatrón "copiar 00–21 dentro de cada proyecto" y la regla de materialización proporcional.
- El maestro sigue siendo la fuente canónica; las copias se declaran espejo físico.
- Se revisa al cerrar FICHA-2 o antes de fusionar a `main`.
- Es reversible a una capa mínima canónica en un solo commit.
- Abre un aprendizaje candidato para el maestro: qué significa "integrar dentro de sí".

### D-A17 · Relectura de D-A06 con la V5.1 (reemplaza a D-A06)
**Fecha:** 2026-10-09
**Decisión:** PH, IT y AT activos. Lo pedagógico (antes C5) y lo comunitario (antes C6) se conservan como focos de gobierno. El Caleidoscopio se registra como evento cuando el contraste entre lentes produzca algo nuevo (Candidato → Reconocido → Validado → Transferido).
**Justificación:** en V5.1 el Caleidoscopio es una propiedad emergente que se reconoce, no un modo que se declara. La intención de D-A06 se conserva.

### D-A18 · Niveles N1–N4 de la activación
**Fecha:** 2026-10-09
**Decisión:** proyecto N3 (D-A05) · producto esperado v1.0 N3, con ruta a N4 · autonomía N3.
**Justificación:** confirma D-A05 en el lenguaje de la V5.1, donde N1–N4 es madurez operacional situada y revisable: autonomía significativa con revisión humana en lo material.

### D-A19 · Activación INTEGRATE autorizada (Paso 4 cerrado)
**Fecha:** 2026-10-09
**Decisión:** se aprueban tal cual el modo INTEGRATE y las redacciones de la ficha compacta: problema, contexto, propósito, métodos, conocimiento, riesgos y gates.
**Consecuencias:**
- La activación se hizo en diálogo humano–IA, sin la app, como prevé el Contrato de Activación V5 §8 y §12.
- La app valida el expediente y lo reimporta sin pérdida.
- El expediente queda en el repositorio:
  - Paquete portable: `00_CONTROL_MAESTRO/Manifiestos/2026-10-09_Paquete_Proyecto_Framework_Boticario_Digital_101_v1_0.json` (y `.zip`, importable en la app).
  - Ficha autorizada: `03_METODOLOGIA_Y_FLUJO_DE_TRABAJO/Ciclo_Vida_Proyectos/2026-10-09_Ficha_Activacion_Compacta_Boticario_Digital_101_v1_0.md`.
  - Copia de este registro: `18_DOCUMENTACION_ACTIVA/Registro_Decisiones/`.
- La hoja de activación borrador (`18_DOCUMENTACION_ACTIVA/Prompts_Activacion/2026-10-09_Hoja_Activacion_INTEGRATE_Boticario_borrador_v0_1.md`) queda reemplazada por la ficha autorizada.
- **Siguiente bloque:** Plano del Buen Vivir · FICHA-2.

---

## Bloque FICHA-2 — Ficha de Saberes v0.2 (Plano del Buen Vivir)

**Insumo:** `00_CONTROL_MAESTRO/Spec_Driven_Development/2026-10-10_Auditoria_Triangulacion_y_Spec_Ficha_Saberes_FICHA_2_v0_2.md` · **Fecha:** 2026-10-10

### D-A20 · Una ficha única completa
**Decisión:** el Boticario, el Recetario y Yocahú usan la misma ficha, con todos sus módulos y sin perfiles por dominio.
**Consecuencias:**
- Ningún módulo se omite. Los vacíos declaran su estado: completo, parcial, no documentado (con fecha de búsqueda) o no aplica (con razón).
- Para publicar se exige un núcleo mínimo: T0, E1, E2, E3, E6, E7, N1, N2 y V1.
- La completitud se mide por módulo.

### D-A21 · Los cuatro niveles de Max-Neef como estructura
**Decisión:** la ficha completa se ordena en Empírico → Pragmático → Normativo → Valores. Las tarjetas de 15 s y 1 min son la puerta de entrada.

### D-A22 · Primer círculo de voces de tradición
**Decisión:** taína y afrocaribeña, Ayurveda, medicina tradicional china, andina y otras indígenas. La biomedicina entra por la evidencia T/E/H (E6).
**Consecuencias:** cada voz tiene su gramática y sus fuentes, y ninguna se traduce en otra (R3). Si una voz no tiene registro para la especie, el campo dice "no documentado"; nunca se rellena por analogía.

### D-A23 · Mapa de 13 dimensiones del bienestar
**Decisión:** el módulo V3 usa los 10 pilares del IBP más las dimensiones ambiental, económica y espiritual de las 8 dimensiones.
**Consecuencias:** V3 registra prácticas de buen vivir, no afirmaciones de salud. Abre una transferencia candidata hacia el Índice de Bienestar.

### D-A24 · Activación proporcional por especie (enmienda a D-A20)
**Fecha:** 2026-10-10
**Decisión:** esquema único, activación proporcional por especie y lente por repositorio.
- Cuatro clases de campo: obligatorio, condicional, opcional y durmiente.
- Cinco estados: activo completo, activo parcial, no documentado, no aplica y durmiente.
- El núcleo mínimo publicable se mantiene.
**Justificación:** prepara la base de conocimiento común futura, compartida entre repositorios, que cada uno interpreta desde su óptica. Los campos durmientes se conservan al compartir (regla I2: preservar lo desconocido).
**Consecuencias:**
- Las etiquetas `sistemas` del REPO pasan a ser disparadores de activación de voces.
- La spec sube a v0.3 (§4.7).

### D-A25 · Activación de módulos durmientes
**Fecha:** 2026-10-10
**Decisión:** las reglas proponen y el humano autoriza. Cada activación queda en el historial T0, con quién, cuándo y qué regla la propuso.

### D-A26 · Custodia por módulo
**Fecha:** 2026-10-10
**Decisión:** diferida. Se decide al integrar las bases entre repositorios.

### D-A28 · Rol de Guersom J. Báez Fonseca (reemplaza a D-A12)
**Fecha:** 2026-10-10
**Decisión:** Guersom J. Báez Fonseca es **coautor**.
**Justificación:** es coautor de la Ficha de Ingrediente Natural v3, la fuente principal del linaje de la Ficha de Saberes, y destinatario de la ficha actualizada del anamú.
**Consecuencias:** la ficha del anamú (FICHA-3) lleva la coautoría de Ricardo Juan Morales De Jesús y Guersom J. Báez Fonseca en T0. El documento fundacional lo registra en §10.
### D-A27 · Canonización del documento fundacional de la Ficha de Saberes
**Fecha:** 2026-10-10
**Decisión:** Ricardo aprueba los documentos de la ficha. El **Documento fundacional v1.0** pasa a **canon vigente** y se usa de ahora en adelante.
- Ubicación: `02_ARQUITECTURA_CONCEPTUAL/Arquitecturas_Referencia/2026-10-10_Documento_Fundacional_Ficha_de_Saberes_v1_0.md`.
- Se aprueban junto con él la Plantilla v0.3, la Spec FICHA-2 v0.3 y el primer de continuidad.
**Consecuencias:** el fundacional gobierna el propósito y los principios, y la spec gobierna la estructura. Cualquier cambio sigue sus reglas de evolución (§9).

### D-A29 · Identificador provisional de especie
**Fecha:** 2026-10-10
**Decisión:** mientras se define el formato definitivo, el identificador es el nombre científico aceptado en minúsculas con guion. Para el anamú: `petiveria-alliacea`.
**Consecuencias:** es provisional. El formato definitivo se decide antes del JSON Schema.

---

## Riesgos abiertos

### R-01 · Menores × contenido sanitario de alto riesgo · **CRÍTICO**
**Origen:** D-A07 + hallazgo de contenido del Bloque 1.
**Descripción:** el catálogo contiene 8 plantas de riesgo alto con contraindicaciones e interacciones medicamentosas de gravedad declarada, y 202 preparaciones con pasos ejecutables (infusión, decocción, tintura). Con audiencia K-12 confirmada, la aplicación puede entregar instrucciones de preparación a una persona menor de edad sin supervisión.
**Estado:** abierto, con avance parcial: D-A09 define el ocultamiento de dosis en modo escolar.
**Debe resolverse en:** G7 (ética y derechos), antes de cualquier trabajo de implementación de la capa pedagógica.
**Opciones a evaluar:** superficie diferenciada por audiencia; ocultar preparaciones de riesgo alto en modo escolar; requerir gesto explícito de adulto; o declarar el proyecto como consulta y no como guía de preparación para audiencias K-12.

---

## Hallazgos del Bloque 1 que originan spec o deuda

| ID | Hallazgo | Destino |
|---|---|---|
| D-05 | Superficie XSS: todo el contenido entra al DOM por `innerHTML` | G9 · bloqueante para v1.0 |
| D-04 | `plantas.json` sin JSON Schema | G5, G9 · **elevado a obligatorio por D-A07** |
| D-06 | Google Fonts y fotos de Wikimedia en tiempo de ejecución | G9 · rompe offline real |
| D-07 | Duplicación de fuentes canónicas (2 JSON, 2 HTML, copias fechadas) | G2 · acta de autoridad documental en apertura |
| D-08 | `LICENSE` ausente; datos de custodia sin licencia declarada | G7 · decisión constitucional de licencia dual |
| D-09 | Accesibilidad no verificada | G8 |
| D-11 | Sin capa i18n | G8, G11 |
| — | Campo `custodios`: obligaciones éticas hacia comunidades | G7 · gobernado por C6 |
| — | Riesgo de daño físico por contenido sanitario | G7 · auditoría `audit:safety` propuesta |
| F-01 | Referencias del catálogo sin revisión por pares (tiendas comerciales como fuente) | G5 · ficha estandarizada |
| F-02 | Afirmaciones sin fuente adyacente; ausencia de fecha de búsqueda | G5 · regla de oro de la ficha |

---

## Estado de los 14 Gates (§10)

| Gate | Estado | Bloqueante |
|---|---|---|
| G1 Propósito | 🟢 | |
| G2 Ubicación | 🟡 | |
| G3 Perfil / Caleidoscopio | 🟢 **cerrado por D-A17** (reemplaza a D-A06) | |
| G4 Metodología | 🟡 en curso (Bloques 2–3) | |
| G5 Evidencia | 🔴 → 🟡 en curso (Bloque FICHA) | |
| G6 IA responsable | 🟡 | |
| G7 Ética y derechos | 🔴 | **Sí — R-01, custodia, licencia** |
| G8 Accesibilidad | 🔴 | |
| G9 Calidad | 🔴 | **Sí — XSS, schema, monolito** |
| G10 Documentación | 🟢 | |
| G11 Wiki / transferencia | 🔴 **elevado por D-A08** | |
| G12 Archivo | 🟡 decidido, no ejecutado | |
| G13 Continuidad | 🟡 | |
| G14 Estabilización | 🔴 destino de la ruta | |

---

*Registro abierto en el Bloque 1. Toda decisión posterior se numera D-Axx y se registra aquí antes de ejecutarse.*
