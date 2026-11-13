---
description: Implementa una spec aprobada, valida y cierra el ciclo
---

Implementa la spec indicada: $ARGUMENTS

Carga y sigue la skill `@implementer`. Lee `docs/project.md`, `docs/architecture.md`, `docs/tech-stack.md` y `docs/conventions.md` cuando aplique; ignora documentos que estén sin completar.

Primero carga la spec y verifica que tenga `status: approved`. Si no está aprobada, detente e informa claramente el estado actual. Implementa únicamente su alcance y no cambies objetivos sin una enmienda explícita.

Ejecuta las validaciones del plan de la spec. Después carga y sigue `@verifier` para contrastar el resultado con los criterios de aceptación. Si hay fallos o bloqueos, no archives la spec: informa los problemas y deja su estado en `ready_for_review`. Si la implementación y la verificación pasan, actualiza el estado a `implemented`, carga y sigue `@closer`, y archiva la spec en `docs/specs/archive/` con estado `archived`.

Entrega los cambios realizados, las validaciones ejecutadas, el resultado de verificación, los riesgos residuales y los siguientes pasos.
