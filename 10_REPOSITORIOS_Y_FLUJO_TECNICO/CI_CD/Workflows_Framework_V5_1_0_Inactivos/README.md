# Workflows del Framework V5.1.0 · inactivos a propósito

Estos cinco archivos vienen del release del Framework. GitHub solo ejecuta los workflows que están en `.github/workflows/` en la raíz. Aquí están guardados como referencia y **no se ejecutan**.

| Workflow | Riesgo si se activara tal cual en el Boticario |
|---|---|
| `framework-v5-pages.yml` | Al hacer push a `main` publicaría la app del Framework y **reemplazaría el sitio del Boticario** en GitHub Pages |
| `framework-v5-release.yml` | Crearía un release "v5.1.0" del Framework dentro del repositorio del Boticario |
| `framework-v5-verify.yml`, `framework-v5-build-preview.yml`, `framework-v5-harden.yml` | Verifican la app en `apps/framework-v5`. Son útiles, pero apuntan a la rama del maestro (`fase3-construccion-v5`) |

Antes de activar cualquiera hay que adaptarlo y registrar la decisión. El candidato natural es `framework-v5-verify.yml`, para validar la app en cada PR.
