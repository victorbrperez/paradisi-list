---
description: Investiga un defecto y crea una spec de corrección
---

Investiga el defecto descrito y prepara una spec de corrección. Reporte: $ARGUMENTS

Lee `docs/project.md`, `docs/architecture.md`, `docs/tech-stack.md` y `docs/conventions.md`. Si alguno conserva placeholders `<...>`, detente sin generar archivos y responde: "Falta contexto del proyecto. Ejecuta `/init-project` primero".

Carga y sigue las skills `@intake` y `@spec-writer`.

Entrevista al usuario para obtener síntoma, pasos de reproducción, esperado frente a actual, frecuencia, impacto, evidencia y entorno afectado. Registra hipótesis de causa raíz solo si hay evidencia. No implementes nada. Crea una spec en `docs/specs/active/<yyyy-mm-dd>-bugfix-<slug>.md` usando `.agents/templates/spec-template.md`, con `type: bugfix`. Usa `draft` si faltan datos de reproducción o evidencia; usa `ready_for_review` solo si existe un diagnóstico razonable y un plan validable.

Al terminar, informa el resumen, la evidencia faltante, la ruta de la spec y su estado.
