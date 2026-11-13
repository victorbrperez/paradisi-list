---
description: Inicia una funcionalidad nueva y crea una spec
---

Inicia una funcionalidad nueva. Solicitud: $ARGUMENTS

Lee `docs/project.md`, `docs/architecture.md`, `docs/tech-stack.md` y `docs/conventions.md`. Si alguno conserva placeholders `<...>`, detente sin generar archivos y responde: "Falta contexto del proyecto. Ejecuta `/init-project` primero".

Carga y sigue las skills `@intake` y `@spec-writer`.

Realiza una entrevista breve para aclarar el problema, el resultado medible, alcance, restricciones, criterios de aceptación y riesgos. No implementes nada. Crea una spec en `docs/specs/active/<yyyy-mm-dd>-feature-<slug>.md` usando `.agents/templates/spec-template.md`, con `type: feature` y estado `draft` si faltan datos críticos o `ready_for_review` si está completa.

Al terminar, informa el resumen, las preguntas pendientes, la ruta de la spec y su estado.
