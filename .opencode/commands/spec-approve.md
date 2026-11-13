---
description: Revisa una spec y apruébala si cumple el checklist
---

Revisa y, si corresponde, aprueba esta spec: $ARGUMENTS

Carga y sigue la skill `@spec-review`. Comprueba objetivo claro, alcance incluido y excluido, criterios de aceptación verificables, plan de validación, riesgos con mitigaciones y plan de rollback. Verifica también que las tecnologías estén definidas en `docs/tech-stack.md` o hayan sido aprobadas explícitamente por el usuario.

Si cumple todos los puntos, actualiza `status: approved` y completa `approval.approved_by` y `approval.approved_at`. Si no cumple, conserva el estado actual y enumera los faltantes concretos. No asumas ni elijas tecnologías o librerías sin aprobación explícita.
