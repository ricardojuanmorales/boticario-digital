# Bitácora de sesión · Boticario Digital 101
**Sesión:** 2026-10-09, 20:59, a 2026-10-10, ~01:30 (hora de Puerto Rico)
**Participantes:** Ricardo Juan Morales De Jesús (autor, decide) · Claude (asistente IA: propone, verifica y redacta)
**Lentes activas:** PH, IT y AT (D-A17) · **Nivel:** N3 (D-A18) · **Modo Framework:** INTEGRATE
**Rama:** `prototipo/framework-v5.1.0` (11 commits sobre `adbb520`; solo local, sin push) · **`main`:** intacto

---

## 1. De qué trató la sesión
La sesión empezó como una evaluación de la ficha del anamú y terminó con:
- **la Ficha de Saberes**, una ficha estandarizada y transdisciplinaria, aprobada y con su documento fundacional en canon;
- **el Framework V5.1 instalado y activado** en el Boticario;
- **el primer caso real llenado**, el anamú.

Hubo un giro central. Ricardo pidió profundizar la ficha **antes** del anamú y situarla en el **ecosistema del buen vivir**. Así nació el Plano del Buen Vivir.

## 2. Recorrido por bloques

| Bloque | Qué pasó | Decisiones |
|---|---|---|
| **FICHA-B1** · diagnóstico del anamú | Se comparó el repo con la ficha actualizada. Se verificaron las 13 referencias: todas existen; hubo 3 hallazgos de rotulado (Conceição es bibliométrico, el autor es Migan y no "Tycko", y el registro NCT está en estado desconocido). Se identificaron 11 problemas en el repo. | D-A09 a D-A12 |
| **Plano del Buen Vivir** | Se leyeron 8 documentos de Ricardo y 7 repositorios. Resultó un archipiélago de apps unidas por el buen vivir; la ficha como nodo de saberes; los 4 niveles de Max-Neef. | D-A13 a D-A15 |
| **FW-1** · prototipo del Framework | Se instaló el release v5.1.0 (718 archivos, SHA-256 verificado) más 3 documentos de fundamento del 8 de octubre. Nada del MVP se sobrescribió y los workflows quedaron inactivos. La app pasó 28 de 28 pruebas y todas sus auditorías. | D-A16 (excepción) |
| **Paso 4** · activación | Se demostró que la activación puede hacerse **en diálogo humano–IA, sin la app**: lo prevé el Contrato de Activación §8 y §12. La app valida el expediente y lo reimporta sin pérdida. | D-A17 a D-A19 |
| **FICHA-2** · auditoría y spec | 35 dimensiones contra 7 fuentes: la v0.1 cubría 14, y los 15 vacíos ya estaban resueltos en fuentes de Ricardo. Salieron la v0.2 y luego la v0.3 con activación proporcional. | D-A20 a D-A26 |
| **Documentación humana** | Se escribieron la plantilla de uso, el primer y el **documento fundacional**, que es hoy canon vigente. | D-A27 a D-A29 |
| **FICHA-3** · anamú | Se llenó la primera ficha real y se emitió un informe de validación: 5 de 5 criterios cumplidos y 6 aprendizajes candidatos. | — |
| **Cierre** | Kit de cierre **guardado en el repositorio** y activable por referencia desde el prompt de activación. Sin ZIP: Ricardo declara superado el §4 del protocolo V4.1.1 (D-A30). | D-A30 |

## 3. Hallazgos principales
1. **El material de Ricardo ya convergía.** La Ficha de Ingrediente v3 sola cubre 24 de 35 dimensiones. La ficha nueva **ensambla**, no inventa.
2. **La activación por IA es una ruta canónica.** El Contrato de Activación V5 prevé que una IA asistente produzca la ficha compacta.
3. **La instalación completa choca con 3 reglas canónicas del Framework**: el antipatrón de copiar 00–21, la materialización proporcional y la capa mínima en INTEGRATE. Se resolvió con una **excepción registrada** (D-A16) y quedó como **aprendizaje candidato** para el maestro (T-002).
4. **El anamú es nativo de Puerto Rico** (GRIN), y las bases taxonómicas **discrepan** en la familia: GBIF dice Phytolaccaceae; APG IV dice Petiveriaceae.
5. **El inventario CIFI 4996 trae afirmaciones sin fuente primaria**: el paso a la leche, el límite de 6 años, la interacción con inmunosupresores y la fitoquímica. Se conservaron como precautorias o se marcaron para verificar.

## 4. Errores de la asistencia IA y su corrección
Se registran por transparencia, y porque Ricardo prefiere entender por qué ocurren los errores.

| Error | Por qué ocurrió | Corrección |
|---|---|---|
| Proponer un prefijo `BD101_` para distinguir documentos | Claude no conocía todavía la regla del Framework: *"las carpetas organizan ubicación; los metadatos, significado"* | Ricardo pidió estudiar el Framework; se retiró la propuesta |
| Crear una subcarpeta sin decisión (`Workflows_Framework_V5_1_0_Inactivos`) | Se priorizó proteger el sitio publicado sin consultar la regla de subcarpetas | Quedó cubierta y declarada en la excepción D-A16 |
| Bloqueos de git (`.lock`) en la carpeta del repo | La carpeta no permitía borrar, y git necesita borrar sus temporales | Se pidió el permiso de borrado y se limpió; se verificó con `git fsck` |
| Tablas Markdown mal formadas en 10 documentos | Faltaba una línea en blanco antes de la tabla; se detectó al generar los PDF | Commit `c2ae7ee`: solo líneas en blanco, ningún cambio de contenido |
| Confundir "35 dimensiones" con "35 campos" en la comunicación | Se habló de la matriz de auditoría sin explicar la diferencia | Se aclaró en el primer y en el fundacional: son 17 módulos y 4 ejes |

## 5. Posible emergencia caleidoscópica (para que Ricardo la reconozca o la descarte, D-A17)
**Candidata:** la **activación proporcional con campos durmientes** ("semilla en latencia"). Surgió del contraste entre tres lentes:
- la necesidad técnica de un esquema único (PH);
- la honestidad sobre los vacíos de evidencia (IT);
- la imagen agroecológica del banco de semillas (AT).

Ninguna lente sola la contenía. Estado propuesto: **Candidato**. Requiere el reconocimiento de Ricardo.

## 6. Lo que queda abierto
- Autorizar la activación del anamú (D-A25).
- Decidir los aprendizajes A1 a A6.
- ¿Ficha v1.0, o un segundo caso alimentario?
- Revisión de la excepción D-A16, **vencida**.
- Formato definitivo del identificador de especie.
- R-01: falta la política general en G7.
- Push de la rama, que hace Ricardo desde VS Code.
- Limpiar la carpeta `_staging` (112 MB).
