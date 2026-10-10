# FICHA-3 · Informe de validación de la Ficha de Saberes v0.3 con el anamú

**Fecha:** 2026-10-10 · **Caso:** *Petiveria alliacea* (anamú) · **Ficha producida:** `13_INVESTIGACION_Y_EVIDENCIA/Sintesis_Evidencia/2026-10-10_Ficha_Saberes_Petiveria_alliacea_Anamu_v0_1.md`
**Pregunta:** ¿la ficha v0.3 funciona con un caso real y difícil? (Documento fundacional §10)

## 1. Resultado frente a los 5 criterios

| # | Criterio | Resultado | Evidencia |
|---|---|---|---|
| 1 | El panel de activación propone bien qué encender | ✅ **Sí.** Las 7 preguntas activaron 15 de los 17 módulos. Dejaron 3 en "no aplica" (P2, P4 y la nutrición de E5) y 4 durmientes (las voces ayurvédica, china y andina, y el eje X4). Las etiquetas del inventario activaron la voz taína y afrocaribeña, como se esperaba. | §A de la ficha |
| 2 | Se alcanza el núcleo publicable con fuentes | ✅ **Sí, como versión parcial.** De los 9 obligatorios, 5 quedan ✅ y 4 ◐ (E2, E3, E6, V1), todos con fuente. | panel |
| 3 | Todo vacío declara su estado | ✅ **Sí.** Ningún campo quedó en blanco. Los 3 ⛔ llevan su razón, cada 💤 está declarado, y hay 4 usos marcados "sin búsqueda". | ficha completa |
| 4 | N2 define qué ve el público escolar (R-01) | ✅ **Sí.** Se definieron 4 superficies, con un mensaje escolar fijo y sin preparaciones ni dosis. **Esto avanza R-01.** | N2 |
| 5 | La carga de trabajo es razonable | ◐ **Razonable porque existía un documento de alta calidad.** El peso está en E6, N1 y E7 (la evidencia). Sin un documento así, cada planta exigiría una búsqueda bibliográfica propia. | ver §3 |

**Veredicto:** la estructura v0.3 **funciona**. No hubo que forzar ningún dato ni dejar ningún vacío sin explicar.

## 2. Lo que la ficha reveló sobre el anamú
- **Familia:** las bases discrepan. GBIF dice Phytolaccaceae; APG IV, según la revisión de 2023, dice Petiveriaceae. Ahora la ficha lo **declara** en vez de esconderlo.
- **Estatus:** **nativa de Puerto Rico** (GRIN). El inventario decía "origen en las Américas" sin precisar.
- **Nombres:** de 4 nombres en el inventario se pasó a 18, incluido el boricua "la yerba que el cabro no masca".
- **Evidencia:** 7 usos tienen búsqueda de evidencia; **4 usos del inventario** (fiebre, malaria, irregularidades menstruales, antimicrobiano) **no la tienen todavía**.
- **Seguridad:** 14 advertencias, cada una con su certeza. **3 afirmaciones del inventario no tienen fuente**: que pasa a la leche, el límite de 6 años y la interacción con inmunosupresores. Se conservan como precautorias (D-A10).
- **Fitoquímica:** los compuestos del inventario no tienen fuente primaria, y hay una posible confusión de nombre (disulfuro o trisulfuro). Las acciones "antitumoral" y "antimicrobiana" se retiraron hasta tener fuente.

## 3. Aprendizajes candidatos para la plantilla (hacia v0.4 o v1.0)
Por la regla del fundacional (§9), ninguno entra en vigor sin tu decisión.

| # | Hallazgo | Propuesta | Tipo de cambio |
|---|---|---|---|
| A1 | Hizo falta declarar una **divergencia entre fuentes** (la familia botánica) | Añadir la marca ⚠️ "divergencia" a E1 y E7 | forma |
| A2 | Hizo falta una **clase de fuente** para inventarios sin cita primaria | En E7, usar el estado de verificación del Framework (`pending_primary_source`) | forma |
| A3 | Usos conocidos por tradición pero **sin búsqueda de evidencia** | Estado de campo "💤 sin búsqueda" dentro de un módulo activo; ya se usó así | forma |
| A4 | La columna **región** de E2 casi nunca tiene fuente | Hacerla opcional | forma |
| A5 | La pregunta "¿se promueve cultivarla?" es también una **cuestión de valores** en una planta de riesgo alto | Separar "documentar el cultivo" (P1) de "promover el cultivo" (decisión en V y N2) | **estructura** |
| A6 | La **reciprocidad** con una tradición colectiva no tiene procedimiento | Abrir un protocolo de reciprocidad comunitaria (G7, D-A06/D-A17 · foco C6) | **estructura** |

## 4. Deuda que deja el caso
- Buscar evidencia E y H para fiebre, malaria, irregularidades menstruales y antimicrobiano.
- Verificar la fitoquímica contra literatura revisada por pares.
- Conseguir una fuente primaria para la atribución taína, o reformularla.
- Confirmar el consentimiento de Guersom como coautor nombrado.
- Licencias del texto (D-08).
- Ejemplar de herbario o foto verificada para subir la certeza de identificación.

## 5. Decisiones que te tocan
1. **Autorizar la activación del anamú** (D-A25). Es el último paso para que la ficha quede vigente.
2. **Los aprendizajes A1 a A6.** Los de forma (A1–A4) pueden entrar en una **plantilla v0.4**. Los de estructura (A5, A6) requieren decisión y actualización de la spec.
3. **¿v1.0 estable?** La estructura funcionó. Puede declararse v1.0 tras aplicar A1–A4, o esperar un segundo caso de especie alimentaria, como el jengibre, que probaría E5 nutrición, P2 y P4, hoy en "no aplica".
