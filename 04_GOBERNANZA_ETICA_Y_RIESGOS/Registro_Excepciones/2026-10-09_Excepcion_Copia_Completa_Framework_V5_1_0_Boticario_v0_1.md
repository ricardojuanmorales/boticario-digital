# Excepción · Copia completa del Framework V5.1.0 en Boticario Digital 101

**Fecha:** 2026-10-09
**Estado:** APROBADA por decisión humana (D-A16)
**Autoridad:** Ricardo Juan Morales De Jesús, autor del Framework y responsable del proyecto
**Ámbito:** repositorio `boticario-digital`, rama `prototipo/framework-v5.1.0` (commit de instalación `14534b9`)
**Modo Framework:** INTEGRATE

## 1. Reglas canónicas que se exceptúan

| Regla | Fuente | Qué dice |
|---|---|---|
| Antipatrón de proliferación | `10_REPOSITORIOS_Y_FLUJO_TECNICO/2026-09-22_Modelo_Portable_Proyecto_Portafolio_Schemas_V5_v0_1.md` §22 | "copiar 00–21 dentro de cada proyecto" |
| Materialización proporcional | `00_CONTROL_MAESTRO/Reglas_Colocacion_Documental/2026-10-06_Regla_Macroestructura_00_21_99_Activacion_Proporcional_V5_1_0.md` | las áreas se materializan cuando existe una función real |
| Capa Framework mínima en INTEGRATE | Modelo Portable §14 | "crear capa Framework mínima" |
| Creación de subcarpetas | `00_CONTROL_MAESTRO/Reglas_Colocacion_Documental/2026-06-05_Protocolo_Manejo_Carpetas_Subcarpetas_Colocacion_Documental_..._v0_2.md` §5–6 | no crear carpeta nueva sin decisión explícita |

## 2. Justificación (D-A14)
Cada repositorio del ecosistema del buen vivir integra el Framework V5.1 dentro de sí **"para poder manejar un lenguaje común y una estructura de trabajo sólida para la integración posterior"**. El Boticario es el prototipo de esa integración. La copia completa permite estudiar cómo funciona el Framework completo dentro de un proyecto real, antes de decidir su forma definitiva.

## 3. Desviaciones concretas que cubre
1. Los 718 archivos del release v5.1.0, más 3 documentos de fundamento y sus índices (maestro `62eb6c8`), están en la raíz del proyecto.
2. Dos renombres en la raíz para no sobrescribir el MVP: `README_Framework_V5_1_0.md` e `index_framework_v5_1_0.html`.
3. Una subcarpeta nueva para guardar inactivos los workflows del Framework: `10_REPOSITORIOS_Y_FLUJO_TECNICO/CI_CD/Workflows_Framework_V5_1_0_Inactivos/`.

## 4. Condiciones y mitigaciones
- **Fuente canónica:** el repositorio maestro sigue siendo la fuente canónica del Framework. Las copias en este proyecto se declaran `tipo_espejo: fisico` y `copia_fisica: true`.
- **Identidad documental:** los documentos del maestro no se editan aquí. Los documentos del Boticario se distinguen por metadatos e índices: las carpetas organizan ubicación y los metadatos organizan significado.
- **Procedencia:** registrada en `00_CONTROL_MAESTRO/Control_Versiones/2026-10-09_Procedencia_Instalacion_Framework_V5_1_0_Prototipo_v0_1.md`, con la huella SHA-256 del release.
- **Actualización:** los cambios futuros del maestro entran solo como transferencia registrada (ver T-001).
- **Protección del MVP:** nada del MVP se sobrescribe y los workflows del Framework permanecen inactivos.

## 5. Revisión
Revisar esta excepción **al cerrar el bloque FICHA-2 o antes de fusionar a `main`**, lo que ocurra primero. Preguntas de revisión:
- ¿El lenguaje común del Framework se usó realmente en el trabajo del Boticario?
- ¿La copia completa generó confusión de identidad o rutas?
- ¿Hubo divergencia entre esta copia y el maestro?

## 6. Reversibilidad
**Sí.** La instalación está aislada en el commit `14534b9`. Reducirla a una capa mínima canónica (núcleo autosostenido, documentos de fundamento, app y áreas 00, 03, 18 y 99) cabe en un solo commit, sin perder historia.

## 7. Aprendizaje candidato para el Framework
La tensión entre D-A14 ("integrar el Framework dentro de cada repositorio") y el antipatrón de copiar 00–21 es un **aprendizaje candidato** para la transferencia simétrica reversible: conviene precisar en el maestro qué significa *integrar dentro de sí* para un ecosistema de repositorios hermanos. No entra al canon de forma automática; requiere contraste y un gate humano.
