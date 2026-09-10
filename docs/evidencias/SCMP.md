# SCMP --- TaskFlow Node.js

## 1. Propósito y alcance
Este plan controla TaskFlow.

## 2. Ítems de configuración
| CI | Ubicación | Control |
|---|---|---|
| API | backend/server.js y backend/db.js | Rama, PR y pruebas |
| Interfaz | frontend/ | Validación funcional y PR |
| Dependencias | backend/package*.json | npm ci y SBOM |
| Esquema | migrations/ | Migraciones SQL numeradas |
| Infraestructura | infra/ | Dockerfile y Compose versionados |
| Automatización | .github/workflows/ci-cd.yml | Pipeline verde |
| Evidencias | docs/evidencias/ | SBOM y ficha por versión |

## 3. Roles
- Responsable de configuración(Cesar Ochoa): mantiene el SCMP y registra líneas base.
- Desarrollador(Carlos Perez): impleta en rama y aporta
- Calidad y revisor(Juan Camilo Rodriguez): revisa el PR de otra persona y verifica el pipeline.

## 4. Control de cambios
1. main no recibe cambios directos.
2. Cada cambio nace en una rama feature/<nombre>.
3. El autor no aprueba su propio Pull Request.
4. Solo se integra con revisión aprobada y pipeline verde.
5. Si cambian dependencias o versión, se regenera el SBOM.
 
## 5. Línea base
- LB-01 / v1.4.0: npm ci, npm test, app ejecutada, SCMP y SBOM aprobados.
 
## 6. Exclusiones
No versionar node_modules/, data/, *.db, secretos, tokens ni archivos personales.
