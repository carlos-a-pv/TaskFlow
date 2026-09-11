# Changelog — TaskFlow

Todas las versiones siguen [SemVer](https://semver.org/lang/es/): `MAJOR.MINOR.PATCH`.

## [1.5.0]
### Added
#### TASKFLOW-101
- Esquema inicial de base de datos (migración `0002_add_due_date.sql`).
- Validación de pruebas.
- POST /api/tasks acepta una fecha opcional.
- POST y GET devuelven la fecha cuando existe.
- Una tarea sin fecha continúa siendo válida.
- Una fecha inválida obtiene HTTP 400.
- La migración conserva las tareas existentes.
- Pruebas anteriores y nuevas quedan verdes.

## [1.4.0] - Baseline de release actual
### Added
- Marcado de tareas como completadas.
- Eliminación de tareas.

## [1.3.0]
### Added
- Listado de tareas ordenado por más recientes.

## [1.2.0]
### Added
- Endpoint de creación de tareas (`POST /api/tasks`).
- Validación de campo `title` requerido.

## [1.1.0]
### Added
- Runner de migraciones (`schema_migrations`), aplicado automáticamente al iniciar.

## [1.0.0]
### Added
- Esquema inicial de base de datos (migración `0001_init.sql`).
- Servicio base Express con health check (`GET /api/health`).

---

## [Unreleased]
### Planned
- `v1.5.0`: campo `fecha_limite` en las tareas — **pendiente, ver `LIVE-DEMO-SCRIPT.md`**.
