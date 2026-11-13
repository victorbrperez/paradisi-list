# Convenciones

## Código
TypeScript con comprobación estricta (`tsconfig.json`). Prettier configura tabs, comillas simples, sin comas finales, ancho de 100 columnas y plugins de Svelte/Tailwind. ESLint aplica sus configuraciones recomendadas para JavaScript, TypeScript y Svelte, junto con compatibilidad con Prettier.

## Nombres
No hay una regla de nombres explícita documentada. En el código actual se observan identificadores en inglés, `camelCase` para variables/funciones y nombres de rutas SvelteKit con el prefijo `+`.

## Estructura de carpetas
Estructura observada: `src/routes/` para páginas, layouts y pruebas E2E cercanas a sus rutas; `src/lib/` para módulos compartidos; `src/lib/server/` para autenticación y base de datos del servidor; `src/lib/assets/` para recursos; `docs/` para documentación del proyecto. Convenciones adicionales de organización: TBD.

## Testing
Vitest ejecuta pruebas de servidor en Node y pruebas de componentes Svelte en Chromium headless; Playwright ejecuta pruebas E2E que coinciden con `**/*.e2e.{ts,js}`. Hay ejemplos en el repositorio. Requisitos de cobertura y criterios adicionales: TBD.

## Seguridad
La configuración obtiene `DATABASE_URL`, `ORIGIN` y `BETTER_AUTH_SECRET` del entorno; la conexión de base de datos y el secreto de autenticación fallan si faltan. `src/env.ts` indica que el secreto de producción debe tener 32 caracteres generados con alta entropía. Otras reglas de validación, gestión de secretos y dependencias: TBD.

## Git y commits

**Branch naming**
- Use lowercase with hyphens (e.g., feature/user-auth)
- Follow the format: type/short-description
- Common branch types:
- feature/ → New feature development (feature/payment-integration)
- bugfix/ → Fixing a bug (bugfix/login-error)
- hotfix/ → Urgent fix on production (hotfix/memory-leak)
- release/ → Preparing a release (release/v1.2.0)
- docs/ → Documentation changes (docs/update-readme)
- refactor/ → Code restructuring (refactor/db-layer)
- test/ → Adding or improving tests (test/api-endpoints)
- chore/ → Maintenance tasks (chore/ci-config)

**Writing commits**
- Start with a type: feat, fix, docs, refactor, test, chore, perf, revert, build, or ci
- Format: <type>(optional-scope): <short-summary>
- Examples:
- feat(auth): add JWT-based login system
- fix(cart): prevent crash on checkout
- docs: update contributing guidelines
- Best practices:
- Use imperative verbs (“add”, “fix”, “update”)
- Keep the subject 50 characters or less
- Write a descriptive body if needed
- Make atomic commits (one logical change per commit)

## Documentación

