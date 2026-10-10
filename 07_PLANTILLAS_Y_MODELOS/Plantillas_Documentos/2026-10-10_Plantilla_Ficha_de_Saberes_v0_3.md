# 🌿 Ficha de Saberes v0.3 · Plantilla de uso

**Para qué sirve:** documentar una especie (planta medicinal, alimento o cultivo) para el Boticario, el Recetario y Yocahú con **una sola ficha**.
**Estado:** APROBADA para uso (decisiones D-A20 a D-A26) · **Spec completa:** `00_CONTROL_MAESTRO/Spec_Driven_Development/2026-10-10_Auditoria_Triangulacion_y_Spec_Ficha_Saberes_FICHA_2_v0_3.md`
**Cómo se ordena:** 4 niveles (Max-Neef) con 17 módulos, más 4 ejes que los atraviesan. Cubre las 35 dimensiones auditadas en FICHA-2 (ver anexo).

---

## Cómo usarla en 5 pasos
1. **Copia** esta plantilla y nómbrala `AAAA-MM-DD_Ficha_Saberes_<especie>_v0_1.md`.
2. **Llena primero el Panel de activación** (§A). Ahí decides qué módulos se encienden para esta planta.
3. **Llena los módulos activos.** Los durmientes se quedan como están, sin escribir nada.
4. **Pon la fuente junto a cada dato** (`[F1]`, `[F2]`…) y regístrala en E7. Si buscaste y no hallaste nada, escribe `🔍 no documentado (búsqueda AAAA-MM-DD)`.
5. **Escribe las tarjetas de 15 s y de 1 min al final**, a partir de lo que llenaste. Son la puerta de entrada de la ficha.

## Leyenda
**Clase del módulo** (lo decide la plantilla):
🔒 **Obligatorio**: sin esto no se publica · ⚡ **Condicional**: pasa a obligatorio si se cumple su condición · ➕ **Opcional** · 💤 **Durmiente**: existe, pero está apagado para esta especie

**Estado del módulo** (lo decides tú, para cada especie):
| Marca | Estado | Qué debe llevar |
|---|---|---|
| ✅ | activo · completo | fuentes |
| ◐ | activo · parcial | qué falta |
| 🔍 | no documentado: **se buscó y no se encontró** | fecha de búsqueda |
| ⛔ | no aplica: **no tiene sentido** para esta especie | razón |
| 💤 | durmiente: **nadie lo ha trabajado todavía** | nada |

## Reglas de oro (las 8 reglas, en corto)
1. **Toda afirmación lleva su fuente**, o dice "no documentado" con la fecha de búsqueda.
2. **Primero tu base curada, después fuentes externas verificables.** Para temas de salud, literatura revisada por pares.
3. **Cada tradición habla en sus propios términos.** Ninguna se traduce en otra, y lo cultural no es lo mismo que lo clínico.
4. **Seguridad con certeza:** marca si cada advertencia está documentada o es precautoria. Las dosis llevan estatus, y las imágenes dicen su origen.
5. **Pide consentimiento antes de nombrar a una persona real.** No publiques coordenadas de recursos vulnerables.
6. **No mezcles fuente, interpretación y decisión.**
7. **Activa solo lo que la especie necesita.** Las reglas proponen y tú autorizas.
8. **No borres versiones viejas:** márcalas como reemplazadas.

---

## §A · Panel de activación de la especie
**Especie:** ______________________ · **Nombre científico:** ______________________ · **Ficha versión:** v0.1 · **Curador/a:** ____________

**Preguntas que encienden módulos (marca sí o no):**
- [ ] ¿Es alimento o condimento? → activa E5 (nutrición), P2 y P4
- [ ] ¿Tiene un uso tradicional con preparación? → activa P3, con estatus de dosis obligatorio
- [ ] ¿Es de riesgo alto o tiene una contraindicación absoluta? → refuerza N1, y N2 debe definir qué ve el público escolar
- [ ] ¿Se cultiva, o se promueve cultivarla? → activa P1, E4 y N3
- [ ] ¿Se cosecha silvestre o está en riesgo? → activa N3
- [ ] ¿La ficha nombra a una persona real? → el consentimiento en V1 pasa a obligatorio
- [ ] ¿El inventario la etiqueta con tradiciones? (`medicina_taína`, `medicina_africana`, `ayurveda`, `medicina_china`…) → activa las voces correspondientes en X1

| Nivel | Módulo | Clase | Estado para esta especie |
|---|---|---|---|
| — | T0 Metadatos y procedencia | 🔒 | |
| Empírico | E1 Identidad taxonómica | 🔒 | |
| Empírico | E2 Nombres y voces | 🔒 | |
| Empírico | E3 Botánica de campo | 🔒 | |
| Empírico | E4 Origen y estatus | ⚡ | |
| Empírico | E5 Composición (fitoquímica · nutrición) | ⚡ | |
| Empírico | E6 Usos y evidencia T/E/H | 🔒 | |
| Empírico | E7 Registro de fuentes | 🔒 | |
| Pragmático | P1 Cultivo y manejo agroecológico | ➕ | |
| Pragmático | P2 Postcosecha e inocuidad | ⚡ | |
| Pragmático | P3 Preparaciones tradicionales | ⚡ | |
| Pragmático | P4 Cocina y recetas | ⚡ | |
| Normativo | N1 Seguridad con certeza | 🔒 | |
| Normativo | N2 Redacción y audiencia | 🔒 | |
| Normativo | N3 Sostenibilidad y trazabilidad | ⚡ | |
| Valores | V1 Custodia y reciprocidad | 🔒 | |
| Valores | V2 Memoria y espiritualidad | ➕ | |
| Valores | V3 Buen vivir | ➕ | |
| Eje | X1 Voces de tradición (5 voces) | ⚡ | |
| Eje | X2 Tarjetas de 15 s y 1 min | ⚡ al publicar | |
| Eje | X3 Estudio y portafolio | ➕ | |
| Eje | X4 Valoración 0–5 | ➕ | |

**Lista para publicar** cuando los 9 🔒 estén en ✅ o ◐, con fuente, y los ⚡ que se activaron estén resueltos.

---

## T0 · Metadatos y procedencia 🔒 · Estado: ___
- Identificador de especie: ________ · Versión: ____ · Estado editorial: borrador / en revisión / validado
- Autoría y curaduría: ________ · Revisores: ________
- Fecha de búsqueda bibliográfica: AAAA-MM-DD
- Historial de cambios y activaciones (quién, cuándo, qué regla lo propuso):
  - AAAA-MM-DD · ________ · ________
- Licencia del contenido y de las imágenes: ________

## NIVEL EMPÍRICO · ¿Qué existe y qué sabemos?

### E1 · Identidad taxonómica 🔒 · Estado: ___
- Nombre científico aceptado y autor: ________ [F_]
- Familia vigente: ________ [F_] · Sinónimos: ________
- Certeza de identificación: alta / media / baja · Voucher o ejemplar de herbario: ________
- ⚠️ **Nombres confusos u homónimos** (especies que comparten nombre común): ________

### E2 · Nombres y voces 🔒 · Estado: ___
| Nombre | Lengua | Región | Comunidad | Fuente |
|---|---|---|---|---|
| | | | | |

### E3 · Botánica de campo 🔒 · Estado: ___
- Morfología: ________ [F_]
- Claves para reconocerla en el campo (olor, hoja, flor…): ________
- Partes usables: ________ · ⚠️ **Partes no usables o tóxicas:** ________
- Imágenes (con origen: foto o ilustración IA, autoría, licencia): ________

### E4 · Origen y estatus ⚡ · Estado: ___
- Centro de origen: ________ · Dispersión y diásporas: ________
- Estatus en PR: nativa / introducida / naturalizada / invasora / en riesgo [F_]
- Hábitat y región biocultural de PR: ________

### E5 · Composición ⚡ · Estado: ___
- **Fitoquímica** (compuesto · clase · fuente): ________
- **Nutrición**, si es alimento (por 100 g y por porción, antinutrientes, biodisponibilidad): ________

### E6 · Usos y evidencia T/E/H 🔒 · Estado: ___
**T** = tradición · **E** = evidencia experimental o preclínica · **H** = evidencia en humanos (di el tipo: ensayo, ex vivo, protocolo, ninguno)
| Condición | Uso tradicional (T) | Experimental (E) | Humana (H) | Redacción permitida | Fuentes |
|---|---|---|---|---|---|
| | | | | | |

### E7 · Registro de fuentes 🔒 · Estado: ___
| ID | Cita | Tipo | DOI/URL | Preparación estudiada | Verificada (fecha) |
|---|---|---|---|---|---|
| F1 | | | | | |

## NIVEL PRAGMÁTICO · ¿Qué podemos hacer?

### P1 · Cultivo y manejo agroecológico ➕ · Estado: ___
- Clima, suelo y luz: ________ · Propagación: ________ · Calendario: ________
- Manejo ecológico de plagas: ________ · Cosecha: ________
- Rol en diseño permacultural (estrato, función: nutre, atrae, repele, cubre): ________

### P2 · Postcosecha e inocuidad ⚡ · Estado: ___
- Secado y conservación: ________ · Vida útil: ________ · Toxinas naturales y cómo mitigarlas: ________

### P3 · Preparaciones tradicionales ⚡ · Estado: ___
| Preparación | Parte | Vía | Pasos | Dosis + **estatus** (validada / tradicional reportada) | Advertencia | Fuente |
|---|---|---|---|---|---|---|
| | | | | | | |

### P4 · Cocina y recetas ⚡ · Estado: ___
- Perfil sensorial (aroma, sabor, textura): ________ · Técnicas: ________
- Sinergias (conectores, contrastes, moduladores): ________
- Recetas vinculadas (id del Recetario): ________

## NIVEL NORMATIVO · ¿Qué queremos hacer?

### N1 · Seguridad con certeza 🔒 · Estado: ___
| Tipo | Descripción | Población | Severidad | Certeza (documentada / precautoria) | Fuente |
|---|---|---|---|---|---|
| Contraindicación | | | | | |
| Interacción | | | | | |
| Efecto adverso | | | | | |

### N2 · Redacción y audiencia 🔒 · Estado: ___
- ✅ Qué **sí** se puede afirmar: ________
- ❌ Qué **no** se debe afirmar: ________
- Qué ve cada público: **escolar** ____ · **general** ____ · **adulto** ____ · **investigación** ____

### N3 · Sostenibilidad y trazabilidad ⚡ · Estado: ___
- Cosecha responsable: ________ · Huella: ________ · Origen y trazabilidad: ________ · Estatus legal: ________

## NIVEL DE VALORES · ¿Qué deberíamos hacer?

### V1 · Custodia y reciprocidad 🔒 · Estado: ___
| Custodio (comunidad o persona) | Rol | ¿Consentimiento? (fecha) | Cómo se reconoce o se retribuye |
|---|---|---|---|
| | | | |

### V2 · Memoria y espiritualidad ➕ · Estado: ___
- Narrativas, refranes, ritual, transmisión familiar (*cultural ≠ clínico*): ________

### V3 · Buen vivir ➕ · Estado: ___
Marca las dimensiones del bienestar con que se relaciona esta especie **como práctica** (cultivarla, cocinarla, compartirla, usarla en un ritual). Esto **no** es una afirmación de salud.
- [ ] Nutrición · [ ] Sueño y descanso · [ ] Actividad física · [ ] Emocional · [ ] Relajación y estrés · [ ] Ocio y juego · [ ] Aprendizaje · [ ] Expresión artística · [ ] Ocupacional · [ ] Comunitario · [ ] **Ambiental** · [ ] **Económico** · [ ] **Espiritual**
- ¿Cómo? ________

## EJES QUE ATRAVIESAN LOS NIVELES

### X1 · Voces de tradición ⚡ · Una línea de estado por voz
| Voz | Estado | Lo que dice, en sus propios términos | Fuente |
|---|---|---|---|
| Taína y afrocaribeña (uso, contexto, custodio) | | | |
| Ayurveda (sabor, cualidades, potencia, efecto posdigestivo, doshas) | | | |
| Medicina china (naturaleza térmica, sabor, meridianos) | | | |
| Andina y otras indígenas (pueblo, nombre originario, categorías propias como cálido/fresco) | | | |
| Biomedicina | → habla en E6 | | |

### X3 · Estudio y portafolio ➕ · Estado: ___
- Preguntas guía para estudio independiente: ________
- Actividad sugerida: ________ · Qué puede guardar la persona en su portafolio: ________

### X4 · Valoración 0–5 ➕ · Estado: ___
(0 = no documentado · 5 = referente) Evidencia ___ · Cultura ___ · Sostenibilidad ___ · Seguridad ___

### X2 · Puerta de entrada ⚡ al publicar (escríbela al final)
- **Tarjeta de 15 s:** qué es + parte usable · su rol · precaución n.º 1 · 3 conexiones
- **Tarjeta de 1 min:** identidad · mejor forma de uso · huerto en una línea · nutriente o bioactivo destacado · precaución principal
- **Etiquetas para filtros:** ________

---

## Anexo · Las 35 dimensiones auditadas y dónde viven en la ficha
| Dimensiones de FICHA-2 | Módulo |
|---|---|
| Metadatos, fecha de búsqueda, historial | T0 |
| Taxonomía, sinónimos, certeza de identificación, voucher, nombres confusos | E1 |
| Nombres por lengua, región y comunidad | E2 |
| Morfología, claves de campo, partes usables y tóxicas, imágenes con origen | E3 |
| Origen y dispersión, estatus ecológico, hábitat y región biocultural | E4 |
| Fitoquímica, nutrición | E5 |
| Usos con evidencia T/E/H | E6 |
| Fuentes como objetos | E7 |
| Cultivo, rol en diseño permacultural, plagas y cosecha | P1 |
| Postcosecha e inocuidad | P2 |
| Preparaciones con estatus de dosis | P3 |
| Cocina, sinergias, recetas vinculadas | P4 |
| Seguridad con certeza, restricciones dietéticas | N1 |
| Redacción permitida, superficie por audiencia | N2 |
| Sostenibilidad, huella, trazabilidad, estatus legal | N3 |
| Custodia y consentimiento | V1 |
| Memoria cultural y espiritualidad | V2 |
| Bienestar y buen vivir | V3 |
| Voces de tradición | X1 |
| Capas de lectura y etiquetas | X2 |
| Estudio independiente, portafolio | X3 |
| Indicadores 0–5 | X4 |
