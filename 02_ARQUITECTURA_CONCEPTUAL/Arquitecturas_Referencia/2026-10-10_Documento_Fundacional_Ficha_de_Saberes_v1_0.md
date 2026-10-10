# 🌿 La Ficha de Saberes · Documento fundacional

**Versión:** 1.0 · **Fecha:** 2026-10-10
**Estado:** ✅ **CANON VIGENTE**, aprobado por Ricardo Juan Morales De Jesús el 2026-10-10 (D-A27). Se usa de ahora en adelante.
**Describe:** la Ficha de Saberes, estructura v0.3 (decisiones D-A20 a D-A26)
**Autoría:** Ricardo Juan Morales De Jesús (autor y curador), con asistencia de IA (Claude). El linaje de autoría está en §3.
**Ubicación canónica:** `02_ARQUITECTURA_CONCEPTUAL/Arquitecturas_Referencia/`

> **Canon no significa eternidad.** Significa referencia vigente, explícita, trazable y revisable. (Framework V5.1)

---

## 1. Qué es la Ficha de Saberes
La Ficha de Saberes es **el documento que reúne todo lo que una comunidad sabe sobre una especie**, sea planta medicinal, alimento o cultivo. Lo reúne sin borrar las diferencias entre las formas de saberlo.

No es una ficha técnica ni una etiqueta de producto. Es **un nodo de saberes**: el punto donde se encuentran la botánica, la evidencia científica, las tradiciones de cura, la cocina, el huerto, la memoria cultural y el buen vivir. Cada saber conserva su voz y su fuente.

Una misma ficha sirve al **Boticario** (plantas medicinales), al **Recetario** (comida como medicina) y a **Yocahú** (agroecología). Cada app la lee desde su óptica, pero la ficha es una sola.

## 2. Por qué existe
Nació de un problema concreto. En Puerto Rico, quienes consultan plantas medicinales, incluidas personas menores de edad, encuentran información dispersa y sin fuentes trazables. Esa información no distingue entre lo que dice la tradición, lo que muestran los estudios de laboratorio y lo que se ha comprobado en personas.

El MVP del Boticario reproducía parte de ese problema. El diagnóstico del anamú (FICHA-B1) lo mostró con claridad:
- daba dosis numéricas sin respaldo clínico;
- citaba tiendas comerciales como fuentes;
- presentaba "anticáncer" como si fuera una indicación;
- usaba una familia botánica desactualizada;
- atribuía saberes culturales sin documentarlos.

La Ficha de Saberes responde con dos compromisos que antes parecían opuestos:
- **respetar profundamente las tradiciones**;
- **ser rigurosamente honesta sobre la evidencia**.

## 3. Origen y linaje
La ficha no se inventó de cero. Ensambla trabajo que ya existía.

| Año | Antecedente | Qué aportó |
|---|---|---|
| 2022 | **Inventario de Plantas Medicinales para Puerto Rico** · CIFI 4996, UPR (Morales De Jesús et al.) | Las 101 plantas, custodios, sistemas médicos, siembra |
| 2026-03 | **Ficha Informativa de Ingrediente Natural v3** · Ricardo Juan Morales De Jesús, Guersom J. Báez Fonseca y el asistente Yocahú | La fuente más completa: 24 de 35 dimensiones; capas de lectura; regla de citación; "cultural ≠ clínico" |
| 2026-04 | **Ficha Técnica de Receta Holística** y el **Módulo de Sinergia** · Recetario Holístico | Voces de Ayurveda y medicina china con gramática propia; cocina y sinergias |
| 2026-04/05 | **MVP del Boticario Digital** (`plantas.json`) | La primera estructura de datos y la experiencia pública |
| 2026 | **Plantilla de proyectos agroecológicos insignia** v1.0 | Territorio, región biocultural, ética de documentación, preguntas de campo |
| 2026-09 | **Ficha integrada del anamú con evidencia clínica** (preparada para Guersom J. Báez Fonseca) | La escala T/E/H, la "redacción permitida" y la fecha de búsqueda |
| 2026-10-09 | **FICHA-B1**: diagnóstico del anamú | Mostró qué faltaba |
| 2026-10-09 | **Plano del Buen Vivir** | Situó la ficha dentro de un ecosistema |
| 2026-10-10 | **FICHA-2**: auditoría por triangulación | 35 dimensiones contra 7 fuentes, que dieron la v0.2 y luego la v0.3 |

## 4. Influencias y fundamentos

### 4.1 Filosóficos
- **Buen vivir.** "Vivir en armonía y equilibrio, con los ciclos de la Madre Tierra, del cosmos, de la vida y de la historia" (Huanacuni, citado en Delgado y Rist, 2016). Es el hilo que une la ficha con el ecosistema.
- **Diálogo de saberes.** Los conocimientos tradicionales y científicos conversan en pie de igualdad, sin que uno absorba al otro (Argueta; Ishizawa; en Delgado y Rist, 2016).
- **Transdisciplinariedad.** Max-Neef ordena el conocimiento en cuatro niveles: qué existe, qué podemos hacer, qué queremos hacer y qué deberíamos hacer. Esa pirámide es **el esqueleto de la ficha**.
- **Conocimiento situado y objetividad fuerte.** Todo saber viene de un lugar y una comunidad, y declararlo lo hace más riguroso, no menos (Rosendahl, Zanella, Rist y Weigelt).
- **Investigación participativa revalorizadora.** Documentar con la comunidad, no sobre ella (Tapia).

### 4.2 Científicos
- **Agroecología, biodiversidad cultural y permacultura.** La planta vive en un territorio, un suelo y un diseño.
- **Etnobotánica.** El uso tradicional se registra como dato cultural valioso.
- **Medicina basada en evidencia.** La escala **T/E/H** distingue la tradición (T), la evidencia experimental o preclínica (E) y la evidencia en humanos (H).

### 4.3 Tradiciones de cura (el primer círculo de voces)
Taína y afrocaribeña (la voz local), Ayurveda, medicina tradicional china, andina y otras indígenas. La biomedicina entra por la evidencia T/E/H.

### 4.4 Bienestar
Los 10 pilares del Índice de Bienestar Personal (Guía Holística de Bienestar y Longevidad), más las dimensiones ambiental, económica y espiritual de las Ocho Dimensiones del Bienestar. Son 13 dimensiones en total.

### 4.5 Metodológicos
- **Framework Genérico V5.1:**
  - el problema situado al centro;
  - las lentes PH, IT y AT;
  - la base de conocimiento común;
  - el portafolio;
  - la activación proporcional;
  - la transferencia simétrica reversible;
  - "el Framework propone, la IA asiste, el humano autoriza".
- **Spec-Driven Development**, según el modelo validado de AI StoryLab 1.

## 5. Principios
Son lo que no cambia aunque cambie la estructura.

1. **Una especie, una ficha.** Todas las apps comparten la misma ficha.
2. **Cada voz en sus términos.** Ninguna tradición se traduce en otra, y lo cultural no es lo mismo que lo clínico. A esto lo llamamos *pluralismo sin equivalencia*.
3. **Cada dato con su fuente.** Si no hay fuente, la ficha dice "no documentado" y la fecha en que se buscó.
4. **Honestidad sobre los vacíos.** Un campo vacío siempre dice por qué lo está: durmiente, no documentado o no aplica.
5. **Seguridad según quién lee.** Lo que ve una persona menor de edad no es lo que ve un investigador.
6. **Consentimiento y reciprocidad.** No se nombra a una persona real sin su permiso, y no se extrae saber sin devolver.
7. **Activación proporcional.** Cada especie enciende lo que necesita; lo demás duerme y puede despertar después.
8. **Decisión humana.** Las reglas y la IA proponen; una persona autoriza lo que importa.
9. **Memoria, no borrado.** Las versiones anteriores se conservan.

## 6. Anatomía de la ficha
La ficha se lee de abajo hacia arriba, como la pirámide de Max-Neef. Cada nivel le da propósito al de abajo.

| Nivel | Pregunta | Módulos |
|---|---|---|
| **Empírico** | ¿Qué existe y qué sabemos? | E1 Identidad taxonómica · E2 Nombres y voces · E3 Botánica de campo · E4 Origen y estatus · E5 Composición · E6 Usos y evidencia T/E/H · E7 Registro de fuentes |
| **Pragmático** | ¿Qué podemos hacer? | P1 Cultivo y manejo agroecológico · P2 Postcosecha e inocuidad · P3 Preparaciones tradicionales · P4 Cocina y recetas |
| **Normativo** | ¿Qué queremos hacer? | N1 Seguridad con certeza · N2 Redacción y audiencia · N3 Sostenibilidad y trazabilidad |
| **Valores** | ¿Qué deberíamos hacer? | V1 Custodia y reciprocidad · V2 Memoria y espiritualidad · V3 Buen vivir |

**Cuatro ejes atraviesan los niveles:**
- **X1 · Voces de tradición:** las cinco voces.
- **X2 · Puerta de entrada:** tarjetas de 15 segundos y de 1 minuto.
- **X3 · Estudio y portafolio.**
- **X4 · Valoración 0–5.**

**T0 · Metadatos y procedencia** lo envuelve todo: versión, autoría, revisores, fecha de búsqueda e historial.

En total son **17 módulos y 4 ejes**, y cubren las 35 dimensiones de la auditoría.

## 7. Activación proporcional
La estructura es completa para todas las especies, pero **cada especie solo enciende lo que necesita**.
- **Clases de módulo:**
  - **obligatorio**: sin él no se publica;
  - **condicional**: pasa a obligatorio si se cumple una condición, como "es alimento";
  - **opcional**;
  - **durmiente**.
- **Estados para cada especie:** activo completo, activo parcial, no documentado (se buscó y no se halló), no aplica (no tiene sentido) y durmiente (nadie lo ha trabajado aún).
- **Núcleo publicable:** T0, E1, E2, E3, E6, E7, N1, N2 y V1.
- **Imagen de trabajo:** el campo durmiente es una semilla en latencia. Está guardado, no se pierde, y germina cuando hay condiciones.

## 8. Quién hace qué

| Rol | Responsabilidad |
|---|---|
| **Curador/a** | Llena la ficha, autoriza qué se activa y responde por su calidad |
| **Revisor/a** | Verifica la evidencia y la seguridad antes de publicar |
| **Custodio** | La comunidad o persona portadora del saber. Da su consentimiento y recibe reconocimiento |
| **IA asistente** | Propone, busca, verifica y redacta borradores. Nunca decide lo material |
| **Comunidad de práctica** | Propone mejoras a la ficha mediante aprendizaje candidato (§9) |

## 9. Cómo se edita y evoluciona
**Los documentos de la ficha, de lo humano a la máquina:**
```text
DOCUMENTO FUNDACIONAL (este)  → el porqué y el qué: propósito, linaje, principios
        ↓
SPEC FICHA-2                  → el cómo: estructura precisa, clases y reglas
        ↓
PLANTILLA                     → el instrumento para llenar una ficha
        ↓
JSON SCHEMA (futuro)          → el contrato que valida la máquina
        ↓
FICHAS DE ESPECIES            → los casos reales, el primero es el anamú
```
**Regla de coherencia:** los cuatro documentos describen la misma ficha. Si divergen, se abre una decisión. Este documento gobierna el **propósito y los principios**; la spec gobierna la **estructura**.

**Tipos de cambio:**
- **De forma** (claridad, ejemplos, redacción): sube la versión menor de este documento (1.0 → 1.1) y se anota en el historial.
- **De estructura** (módulos, clases, reglas, voces): requiere una decisión D-Axx registrada, la actualización de la spec y de la plantilla, y un gate humano. Sube la versión mayor (1.x → 2.0).
- **De principios** (§5): requiere el gate humano de Ricardo y la revisión de la comunidad de práctica.

**Del caso al canon.** Lo que se aprende al llenar una ficha (el anamú es el primero) entra como **aprendizaje candidato**. Luego pasa por el contraste y el gate humano, y entonces se integra o se descarta. Nada entra al canon de forma automática. Es la transferencia simétrica reversible del Framework.

**Memoria.** Ninguna versión se borra; las reemplazadas se marcan como tales.

## 10. Primer caso de aplicación: el anamú
**Por qué el anamú.** Es el caso más exigente, y si la ficha funciona con él, funcionará con casi cualquier otra especie:
- es de **riesgo alto** (contraindicado en el embarazo, audiencia K-12);
- tiene **evidencia rica y verificada**: un ensayo clínico, estudios ex vivo y un protocolo registrado;
- tiene **presencia cultural profunda** en las tradiciones taína y afrocaribeña de Puerto Rico;
- ya existe un **documento actualizado** de alta calidad.

**FICHA-3 debe demostrar que:**
1. el panel de activación propone correctamente qué módulos encender;
2. se alcanza el núcleo publicable con fuentes;
3. todo vacío declara su estado;
4. N2 define qué ve el público escolar, lo que avanza el riesgo R-01;
5. la carga de trabajo es razonable.

**Autoría de la ficha del anamú:** Ricardo Juan Morales De Jesús y Guersom J. Báez Fonseca, **coautores** (D-A28).

**Al cerrar:** con lo que aprendamos, la estructura pasa a **v1.0 estable** o a una v0.4 con ajustes.

## 11. Glosario
- **T/E/H:** tradición, evidencia experimental y evidencia en humanos.
- **Voz:** una tradición de saber con su propia gramática y sus fuentes.
- **Activación proporcional:** cada especie enciende solo los módulos que necesita.
- **Durmiente:** un módulo que existe pero nadie ha trabajado todavía.
- **Núcleo publicable:** los 9 módulos sin los cuales una ficha no se publica.
- **Custodio:** la comunidad o persona portadora del saber.
- **Lente:** la óptica con que cada app lee la misma ficha.
- **Canon:** la referencia vigente y revisable, no una verdad eterna.

## 12. Historial

| Versión | Fecha | Cambio | Decisión |
|---|---|---|---|
| 1.0 | 2026-10-10 | Primera redacción, aprobada como canon vigente; coautoría de Guersom en §10 | D-A27 · D-A28 |

## Referencias
- Delgado, F. y Rist, S. (Eds.) (2016). *Ciencias, diálogo de saberes y transdisciplinariedad: aportes teórico metodológicos para la sustentabilidad alimentaria y del desarrollo*. AGRUCO / Plural editores. ISBN 978-99954-1-728-4. Incluye: Max-Neef, "Los cimientos de la transdisciplinariedad"; Argueta, "El diálogo de saberes, una utopía realista"; Ishizawa, "Comunidades epistémicas para el diálogo de saberes"; Tapia, "El diálogo de saberes y la investigación participativa revalorizadora"; Rosendahl, Zanella, Rist y Weigelt, "Conocimiento científico situado: la objetividad fuerte en transdisciplinariedad".
- Morales De Jesús, R. J. et al. (2022). *Inventario de Plantas Medicinales para Puerto Rico*. CIFI 4996. Universidad de Puerto Rico.
- Morales De Jesús, R. J., Báez Fonseca, G. J. y Yocahú (2026). *Ficha Informativa de Ingrediente Natural: Plantilla Maestra Extendida v3.0*.
- Morales De Jesús, R. J. (2026). *Recetario Holístico Transdisciplinario v1.1*; *Guía Básica de Nutrición Humana y Guía Holística de Bienestar y Longevidad v1.1*; *Plantilla maestra para inventario de proyectos agroecológicos insignia v1.0*; *Elementos de un hábitat humano sostenible*.
- *Anamú: ficha integrada con matriz de usos, evidencia experimental, evidencia clínica humana y seguridad* (2026, búsqueda al 29 de septiembre).
- Framework Genérico V5.1.0: Arquitectura Conceptual Integrada v1.0; Contrato de Base de Conocimiento común V5; Regla de Macroestructura V5.1; Modelo Portable de Proyecto.
