# FICHA-2 · Auditoría por triangulación y Ficha de Saberes v0.2 (spec candidata)

**Proyecto:** Boticario Digital 101 · ecosistema del buen vivir
**Fecha:** 2026-10-10
**Estado:** CANDIDATA. Espera decisiones de Ricardo (§6).
**Tipo SDD:** spec de objeto de dominio, la primera del Boticario.
**Lentes:** PH, IT y AT (D-A17) · **Nivel:** N3 (D-A18)
**Insumos auditados:**
- **v0.1:** la propuesta de 11 módulos (FICHA-B1 §6).
- **DOCX:** la ficha integrada del anamú.
- **ING:** la Ficha Informativa de Ingrediente Natural v3.
- **REC:** la Ficha Técnica de Receta Holística.
- **AGRO:** la Plantilla de proyectos agroecológicos insignia.
- **REPO:** `boticario_101_plantas_completo.json`.
- **FW:** los esquemas y contratos del Framework V5.1.
- **Max-Neef:** sus cuatro niveles, en Delgado y Rist (2016).

---

## 1. Resultado en tres líneas
1. La v0.1 cubre por completo **14 de 35 dimensiones**, 6 de forma parcial, y le faltan 15. Es una buena ficha de botica, pero todavía no es una ficha del buen vivir.
2. **Los 15 vacíos ya están resueltos en al menos una de tus propias fuentes.** La v0.2 no inventa: ensambla lo que ya creaste.
3. La pirámide de Max-Neef ordena todo **sin añadir campos**, y aporta el nivel de *valores*, que ninguna plantilla técnica tenía completo.

## 2. Matriz de triangulación
● cubre · ◐ parcial · ○ ausente. La columna *Nivel* ubica cada dimensión en la pirámide de Max-Neef.

| # | Dimensión | Nivel | v0.1 | DOCX | ING | REC | AGRO | REPO | FW | Dónde ya lo resolviste |
|---|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|---|
| 1 | Metadatos: versión, estado, revisores, historial | transversal | ● | ◐ | ● | ○ | ◐ | ● | ● | ING 12.1 · REPO meta · FW maturityStatus |
| 2 | Fecha de búsqueda y verificación | transversal | ● | ● | ◐ | ○ | ○ | ○ | ● | DOCX §10 · FW provenance.migrationDate |
| 3 | Identidad taxonómica y sinónimos | empírico | ● | ● | ● | ○ | ○ | ◐ | ○ | ING 0.0.1 · DOCX §1 (Petiveriaceae) |
| 4 | Certeza de identificación y voucher de herbario | empírico | ○ | ◐ | ● | ○ | ○ | ○ | ○ | ING 0.0.1.4–0.0.1.5 |
| 5 | Nombres confusos u homónimos | empírico | ○ | ○ | ● | ○ | ○ | ○ | ○ | ING 0.0.0.5 |
| 6 | Nombres por lengua, región, comunidad y fuente | empírico | ● | ◐ | ● | ◐ | ○ | ◐ | ○ | ING 0.0.0 · REC 2.2 |
| 7 | Morfología y claves de campo | empírico | ● | ● | ● | ○ | ○ | ● | ○ | ING 0.1.0 · REPO botanica |
| 8 | Partes usables y partes no usables o tóxicas | empírico | ◐ | ◐ | ● | ○ | ○ | ◐ | ○ | ING 0.0.2.0–0.0.2.1 |
| 9 | Origen, dispersión, diásporas y colonialidad | empírico | ○ | ○ | ● | ● | ○ | ◐ | ○ | ING 2.0 · REC 7 |
| 10 | Estatus ecológico: nativa, introducida, invasora, en riesgo | empírico | ○ | ○ | ● | ○ | ◐ | ○ | ○ | ING 2.1.2 · AGRO 5.1 |
| 11 | Hábitat, región biocultural y microclima de PR | empírico | ● | ○ | ◐ | ○ | ● | ● | ○ | AGRO §1 · REPO habitats_pr |
| 12 | Fitoquímica | empírico | ● | ○ | ● | ● | ○ | ● | ○ | ING 9.1.1 · REC 5 |
| 13 | Nutrición, antinutrientes y biodisponibilidad | empírico | ○ | ○ | ● | ● | ◐ | ○ | ○ | ING 9 · REC 5 |
| 14 | Usos por condición con evidencia T/E/H | empírico | ● | ● | ● | ◐ | ○ | ◐ | ○ | DOCX §4 · ING 10.0–10.1 |
| 15 | Redacción permitida: qué sí y qué no afirmar | normativo | ● | ● | ● | ○ | ○ | ○ | ○ | DOCX §4.2 · ING 10.2 |
| 16 | Seguridad con nivel de certeza | normativo | ● | ● | ● | ◐ | ○ | ◐ | ○ | DOCX §4.3 · ING 11 · D-A10 |
| 17 | Restricciones dietéticas prácticas (diabetes, renal) | normativo | ○ | ◐ | ● | ◐ | ○ | ○ | ○ | ING 11.1–11.2 |
| 18 | Preparaciones tradicionales con estatus de dosis | pragmático | ● | ● | ◐ | ○ | ○ | ● | ○ | DOCX §7 · ING 10.0.4 · D-A09 |
| 19 | Cocina: perfil sensorial, técnicas y sinergias | pragmático | ○ | ○ | ● | ● | ○ | ○ | ○ | ING 8 · REC 11 |
| 20 | Recetas vinculadas (comida como medicina) | pragmático | ○ | ○ | ● | ● | ◐ | ○ | ○ | ING 2.2.3, 8.3 · REC |
| 21 | Cultivo, propagación y condiciones | pragmático | ● | ○ | ● | ○ | ● | ● | ○ | ING 3–4 · AGRO §4 · REPO siembra |
| 22 | Rol en diseño permacultural o agroforestal | pragmático | ○ | ○ | ● | ○ | ● | ○ | ○ | ING 3.3 · AGRO 4.4 |
| 23 | Manejo de plagas, calendario, cosecha y postcosecha | pragmático | ◐ | ○ | ● | ○ | ● | ◐ | ○ | ING 5–7 · AGRO 4.6 |
| 24 | Sostenibilidad, huella, trazabilidad y estatus legal | normativo | ◐ | ○ | ● | ● | ● | ◐ | ○ | ING 0.1.2 · REC 9 · AGRO 5.6 |
| 25 | Custodia, consentimiento y reciprocidad | valores | ● | ○ | ○ | ○ | ● | ● | ◐ | AGRO §20 · REPO custodios |
| 26 | Memoria cultural, narrativas, ritual y espiritualidad | valores | ◐ | ○ | ● | ◐ | ● | ● | ○ | ING 2.2.1 · AGRO 2.5, 9.4 |
| 27 | Voces de tradición con gramática propia | transversal | ○ | ○ | ○ | ● | ○ | ◐ | ○ | REC 6 (Ayurveda, MTC, naturismo) |
| 28 | Capas de lectura y etiquetas para filtros | transversal | ○ | ○ | ● | ○ | ◐ | ○ | ○ | ING 1.0–1.2 · AGRO §16 |
| 29 | Superficie por audiencia (K-12, adulto, investigación) | normativo | ◐ | ◐ | ○ | ◐ | ○ | ○ | ○ | D-A09 · R-01 · REC 1.1 |
| 30 | Bienestar y buen vivir (pilares, salud planetaria) | valores | ○ | ○ | ○ | ◐ | ● | ○ | ○ | AGRO §9 · REC 5 (salud planetaria) |
| 31 | Estudio independiente: preguntas guía y actividades | transversal | ○ | ○ | ○ | ○ | ● | ○ | ○ | AGRO §15 |
| 32 | Indicadores y matriz de valoración 0–5 | transversal | ○ | ○ | ○ | ● | ● | ○ | ○ | AGRO §13 · REC 10 |
| 33 | Fuentes como objetos (tipo, nivel, preparación estudiada, estado) | empírico | ● | ● | ● | ◐ | ◐ | ○ | ● | DOCX §10 · ING 12 · FW common-knowledge-item |
| 34 | Imágenes con origen declarado (foto o IA) | transversal | ◐ | ◐ | ○ | ○ | ◐ | ◐ | ○ | D-A11 · AGRO §14 |
| 35 | Portafolio y anotaciones personales | transversal | ○ | ○ | ○ | ○ | ○ | ○ | ● | FW portfolio.schema |
| | **Cobertura plena / parcial / ausente** | | 14/6/15 | 8/7/20 | 24/3/8 | 8/8/19 | 10/7/18 | 8/10/17 | 4/1/30 | |

**Cómo leerla:** tu **Ficha de Ingrediente v3 es la fuente más completa (24 de 35)**. El DOCX del anamú aporta el rigor de la evidencia. La Plantilla agroecológica aporta territorio, comunidad, ética y estudio. El Framework aporta el portafolio y el modelo de fuentes.

## 3. Hallazgos de la auditoría
1. **Falta un control de seguridad que la v0.1 no vio:** los *nombres confusos* y las *partes tóxicas* (ING 0.0.0.5 y 0.0.2.1). En plantas medicinales, confundir dos especies que comparten nombre común es un riesgo real, y pesa más con audiencia K-12.
2. **Una especie, muchas fichas.** La ficha de planta y la de ingrediente comparten la mayor parte de los campos: identidad, nombres, botánica, origen, composición, usos, seguridad, cultura y fuentes. Conviene un **núcleo común** con **perfiles de dominio** encima.
3. **La regla de fuentes ya es la misma en tres lugares:**
   - el DOCX pone la fuente junto a la afirmación;
   - ING 12.2 exige que toda afirmación tenga fuente, si no se marca "No documentado / requiere verificación", y fija la prioridad: base interna primero, externa verificable después;
   - el Framework distingue fuente, interpretación, decisión y canon, y les da estados de verificación.

   La v0.2 las unifica.
4. **El "pluralismo sin equivalencia" ya tenía antecedente en tu propia plantilla:** ING 2.2.1.5 dice *"cultural ≠ clínico"*.
5. **Las voces de tradición solo aparecen con gramática propia en REC 6** (Ayurveda, MTC, naturismo). En el REPO, los "sistemas" son etiquetas sin campos. La v0.2 las convierte en un eje transversal.
6. **Las capas de lectura (ING 1.0–1.2) resuelven la sobrecarga.** La ING v3 tiene unos 200 campos. Sin capas ni núcleo mínimo, la ficha sería inmanejable para K-12 y para quien contribuye.
7. **AGRO trae lo que el Boticario necesita para ser comunitario:**
   - ética de documentación: consentimiento, no publicar coordenadas sensibles, reciprocidad (§20);
   - preguntas guía de campo (§15);
   - región biocultural (§1).
8. **Lo que no entra en la ficha de especie:** la gerencia y el mercadeo de REC §1 (costos, márgenes, storytelling). Pertenecen a la ficha de receta.
9. **El registro de fuentes puede usar el esquema `common-knowledge-item` del Framework:** tipo, procedencia, estado de madurez y de verificación, anotaciones. Así las fuentes del Boticario son interoperables con la Base de Conocimiento común desde el primer día.
10. **El portafolio solo existe en el Framework.** La ficha debe declarar qué puede hacer la persona con ella (anotar, guardar en el herbario, registrar evidencia), y eso se guarda con el esquema de portafolio del Framework (D-A15).

## 4. Ficha de Saberes v0.2

### 4.1 Arquitectura: una especie, muchas fichas
```text
ESPECIE (identificador común, nombre científico aceptado)
├── núcleo común ─────────── lo que toda ficha comparte
├── perfil Planta medicinal ─ Boticario
├── perfil Ingrediente ────── Recetario
└── perfil Cultivo ────────── Yocahú
```
Cada app conserva su ficha y su voz. El identificador común las conecta, como en el "Una especie, muchas puertas" del Plano.

### 4.2 Estructura: los cuatro niveles de Max-Neef
**T0 · Metadatos y procedencia** (transversal): versión, estado, autoría, revisores, fecha de búsqueda, historial de cambios, nivel de evidencia por sección y licencias.

**EMPÍRICO · ¿qué existe y qué sabemos?**
| ID | Módulo | Contenido | Viene de |
|---|---|---|---|
| E1 | Identidad taxonómica | nombre aceptado y autor, familia vigente, sinónimos, **certeza de identificación**, voucher, **nombres confusos** | DOCX · ING 0.0 |
| E2 | Nombres y voces | nombre × lengua × región × comunidad × fuente | v0.1 M2 · ING 0.0.0 |
| E3 | Botánica de campo | morfología, claves, **partes usables y partes tóxicas**, imágenes con origen declarado | REPO · ING 0.0.2, 0.1 · D-A11 |
| E4 | Origen y estatus | centro de origen, dispersión, diásporas, **nativa, introducida o invasora**, hábitat y región biocultural de PR | ING 2.0–2.1 · AGRO §1 |
| E5 | Composición | fitoquímica; **nutrición, antinutrientes y biodisponibilidad** cuando es alimento | ING 9 · REC 5 |
| E6 | Usos y evidencia | por condición: T, E y H, tipo de estudio, preparación estudiada, resultado frente a placebo | DOCX §4 · ING 10 |
| E7 | Registro de fuentes | id, tipo, DOI o URL, preparación estudiada, fecha y estado de verificación (esquema FW) | DOCX §10 · ING 12 · FW |

**PRAGMÁTICO · ¿qué podemos hacer?**
| ID | Módulo | Contenido | Viene de |
|---|---|---|---|
| P1 | Cultivo y manejo agroecológico | condiciones, propagación, calendario, manejo de plagas, cosecha, **rol en diseño permacultural** | ING 3–6 · AGRO §4 · REPO |
| P2 | Postcosecha e inocuidad | conservación, secado, vida útil, toxinas naturales y cómo mitigarlas | ING 7 |
| P3 | Preparaciones tradicionales | forma, parte, vía, pasos; dosis **con estatus** (validada o tradicional reportada) | DOCX §7 · REPO · D-A09 |
| P4 | Cocina y recetas | perfil sensorial, técnicas, **sinergias**, recetas vinculadas por id | ING 8 · REC 11 |

**NORMATIVO · ¿qué queremos hacer?**
| ID | Módulo | Contenido | Viene de |
|---|---|---|---|
| N1 | Seguridad con certeza | contraindicaciones, interacciones, efectos y restricciones dietéticas, cada uno documentado o precautorio | DOCX §4.3, §5 · ING 11 · D-A10 |
| N2 | Redacción y audiencia | qué sí y qué no afirmar; qué ve cada público: escolar, general, adulto, investigación | DOCX · ING 10.2 · R-01 |
| N3 | Sostenibilidad y trazabilidad | cosecha responsable, huella, origen, estatus legal | ING 0.1.2 · REC 9 · REPO |

**VALORES · ¿qué deberíamos hacer?**
| ID | Módulo | Contenido | Viene de |
|---|---|---|---|
| V1 | Custodia y reciprocidad | custodios **con consentimiento**, atribución, reciprocidad y ética de documentación | AGRO §20 · REPO custodios |
| V2 | Memoria y espiritualidad | narrativas, refranes, ritual y transmisión familiar (*cultural ≠ clínico*) | ING 2.2.1 · AGRO 2.5 |
| V3 | Buen vivir | vínculo con los pilares de bienestar, la relación con la tierra y el hábitat sostenible | AGRO §9 · Guía holística · Hábitat sostenible |

### 4.3 Ejes transversales
| ID | Eje | Qué hace |
|---|---|---|
| X1 | Voces de tradición | Cada voz tiene su propia gramática y sus fuentes. Por ejemplo, el Ayurveda usa sabor, potencia y efecto posdigestivo; la medicina china, naturaleza térmica y sabor; la voz taína y afrocaribeña, uso, contexto y custodios. La biomedicina habla mediante E6 (T/E/H). |
| X2 | Capas de lectura | Tarjeta de 15 s → tarjeta de 1 min → ficha completa → estudio independiente, más etiquetas para filtros (ING 1.0–1.2) |
| X3 | Estudio y portafolio | Preguntas guía y actividades (AGRO §15). Lo que la persona anota se guarda en su portafolio con el esquema del Framework. |
| X4 | Valoración 0–5 (opcional) | Matriz de presencia por dimensión (AGRO §13) |

### 4.4 Reglas transversales
| Regla | Enunciado | Origen |
|---|---|---|
| R1 | Toda afirmación apunta a un id de E7, o declara "No documentado / requiere verificación (búsqueda AAAA-MM-DD)" | DOCX · ING 12.2.2 |
| R2 | Prioridad de fuentes: base interna curada primero, externa verificable después; para salud, revisada por pares | ING 12.2.1 · DOCX §9 |
| R3 | Pluralismo sin equivalencia: ninguna voz se traduce en otra, y *cultural ≠ clínico* | Plano · ING 2.2.1.5 |
| R4 | Certeza en seguridad, estatus de dosis y origen de imagen | D-A09 · D-A10 · D-A11 |
| R5 | Consentimiento antes de nombrar a personas reales; sin coordenadas exactas de recursos vulnerables | AGRO §20 |
| R6 | Fuente ≠ interpretación ≠ decisión ≠ canon; estados: propuesto → revisado → validado → referencia → reemplazado | FW Contrato Base de Conocimiento |
| R7 | Activación proporcional: núcleo mínimo más el perfil; no todos los módulos para todas las especies | FW Regla de Macroestructura V5.1 |
| R8 | Las versiones reemplazadas se marcan, no se borran | FW Protocolo de colocación §11 |

### 4.5 Núcleo mínimo publicable y perfiles
- **Núcleo mínimo** (sin esto, una ficha no se publica): T0, E1, E2, E3, E6, E7, N1, N2, V1.
- **Perfil Planta medicinal (Boticario):** núcleo + E4, E5 (fitoquímica), P1, P3, N3, V2, V3, X1, X2, X3.
- **Perfil Ingrediente (Recetario):** núcleo + E4, E5 (nutrición), P2, P4, X1, X2.
- **Perfil Cultivo (Yocahú):** núcleo + E4, P1, P2, N3, V2.

### 4.6 De la v0.1 a la v0.2
| v0.1 | → v0.2 |
|---|---|
| M0 Metadatos | T0 |
| M1 Identidad | E1, con certeza y nombres confusos |
| M2 Nombres y culturas | E2 y el eje X1 |
| M3 Botánica | E3 y E4 |
| M4 Matriz T/E/H | E6 y N2 |
| M5 Seguridad | N1 |
| M6 Preparaciones | P3 |
| M7 Fitoquímica | E5 |
| M8 Cultivo | P1 (y P2, nuevo) |
| M9 Custodia | V1 |
| M10 Fuentes | E7 |
| *nuevos* | P4 · N3 · V2 · V3 · X2 · X3 · X4 |

## 5. Siguiente paso
**FICHA-3 · validar la v0.2 con el anamú.** Se llena el núcleo mínimo y el perfil de planta medicinal con el DOCX, el REPO y tus fuentes, y se registra lo que la ficha no pudo contener. Solo después se escribe el JSON Schema (D-04), que es contrato obligatorio por D-A07.

## 6. Decisiones para Ricardo
1. **Arquitectura:** ¿núcleo común más perfiles de dominio, es decir, una especie con muchas fichas?
2. **Estructura:** ¿los cuatro niveles de Max-Neef como esqueleto de la ficha completa?
3. **Primer círculo de voces de tradición** para el eje X1.
4. **Escala de bienestar** para V3.

**Pendientes, sin urgencia:**
- D-A12: la Ficha de Ingrediente v3 nombra a Guersom J. Báez Fonseca **coautor**.
- Identificador común de especie. Propuesta: el nombre científico aceptado, verificado contra una base taxonómica abierta.
