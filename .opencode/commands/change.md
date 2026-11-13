---
description: Prepara un cambio de funcionalidad existente y crea una spec
---

Prepara un cambio sobre funcionalidad existente. Solicitud: $ARGUMENTS

Lee `docs/project.md`, `docs/architecture.md`, `docs/tech-stack.md` y `docs/conventions.md`. Si alguno conserva placeholders `<...>`, detente sin generar archivos y responde: "Falta contexto del proyecto. Ejecuta `/init-project` primero".

Carga y sigue las skills `@intake` y `@spec-writer`.

Entrevista al usuario sobre el comportamiento actual y el deseado, áreas afectadas, compatibilidad, criterios de aceptación, pruebas y riesgo de regresión. No implementes nada. Crea una spec en `docs/specs/active/<yyyy-mm-dd>-change-<slug>.md` usando `.agents/templates/spec-template.md`, con `type: change` y estado `draft` si faltan datos críticos o `ready_for_review` si está completa.

Al terminar, informa el resumen, los datos pendientes, la ruta de la spec y su estado.
