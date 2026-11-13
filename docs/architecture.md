# Arquitectura

## Visión general
Aplicación SvelteKit con rutas en `src/routes`, lógica de servidor en `src/lib/server` y acceso a datos mediante Drizzle sobre SQLite/libSQL. Better Auth se integra en el hook del servidor. El repositorio conserva contenido de scaffold/demo; la arquitectura funcional final del producto está TBD.

## Componentes
| Componente | Responsabilidad | Ubicación |
|---|---|---|
| Rutas y páginas | Interfaz principal y páginas de demo de Playwright y Better Auth. | `src/routes/` |
| Hook del servidor | Obtiene la sesión, la adjunta al contexto local de la petición y delega en el handler de Better Auth. | `src/hooks.server.ts` |
| Autenticación | Configura Better Auth con almacenamiento Drizzle y email/contraseña. | `src/lib/server/auth.ts` |
| Acceso a datos | Crea el cliente libSQL y la instancia Drizzle; declara las tablas de tareas y autenticación. | `src/lib/server/db/` |
| Pruebas | Pruebas de unidad/componentes y una prueba E2E de ejemplo. | `src/lib/vitest-examples/`, `src/routes/demo/` |

## Flujo de datos
En las peticiones del servidor, el hook consulta la sesión de Better Auth y, si existe, asigna sesión y usuario a `event.locals`; después llama al handler de SvelteKit de Better Auth. La página de demo de autenticación redirige a usuarios no autenticados a login y su acción de salida cierra la sesión. La configuración de datos crea el cliente libSQL desde `DATABASE_URL` y conecta Drizzle al esquema. No se observó un flujo de lectura/escritura de tareas desde las rutas; el flujo de producto queda TBD.

## Decisiones (ADR breves)
- TBD. No hay ADR ni justificación de alternativas en la documentación revisada.

## Restricciones
Configuración observada: dialecto SQLite en Drizzle, TypeScript estricto y adapter-auto de SvelteKit. Restricciones adicionales de negocio, rendimiento y despliegue: TBD.

## Integraciones externas
Better Auth se integra con SvelteKit y Drizzle; el backend de datos se selecciona mediante `DATABASE_URL`. No se identificaron otros servicios o APIs externos configurados. Proveedor y entornos reales: TBD.
