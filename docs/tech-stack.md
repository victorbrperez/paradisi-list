# Tech Stack

## Lenguajes y versiones
- TypeScript — `^6.0.3` (rango declarado en `package.json`).
- Node.js y npm — versión: TBD.

## Frameworks y librerías
| Nombre | Versión | Propósito |
|---|---|---|
| Svelte | `^5.57.2` | Componentes de interfaz. |
| SvelteKit | `^3.0.0` | Aplicación web y enrutamiento. |
| Tailwind CSS | `^4.3.0` | Estilos; integrado mediante el plugin de Vite. |
| Vite | `^8.3.0` | Desarrollo y build. |
| Drizzle ORM | `^0.45.2` | Acceso a datos y esquema SQLite. |
| `@libsql/client` | `^0.17.3` | Cliente de base de datos compatible con libSQL. |
| Better Auth | `^1.6.24` | Autenticación; email y contraseña están habilitados en la configuración. |

## Almacenamiento
Drizzle está configurado con dialecto SQLite y el cliente libSQL; `DATABASE_URL` proporciona la URL. El proveedor concreto y los entornos donde se usa están TBD. No se encontró configuración de caché, colas u object storage.

## Infraestructura y despliegue
SvelteKit usa `adapter-auto`. El destino de despliegue, los contenedores, CI/CD y los entornos configurados están TBD; no se encontró configuración de proveedor o pipeline.

## Herramientas de desarrollo
Vite (`dev`, `build`, `preview`); ESLint; Prettier con plugins de Svelte y Tailwind; `svelte-check`; Vitest para pruebas unitarias/componentes en navegador y servidor; Playwright para E2E; Drizzle Kit para tareas de base de datos. El proyecto declara npm y contiene `package-lock.json`.

## Servicios externos
No se identificaron APIs o proveedores SaaS configurados. El servicio concreto detrás de `DATABASE_URL` está TBD.

## Restricciones
No se encontraron restricciones tecnológicas o requisitos de licencia documentados; TBD.
