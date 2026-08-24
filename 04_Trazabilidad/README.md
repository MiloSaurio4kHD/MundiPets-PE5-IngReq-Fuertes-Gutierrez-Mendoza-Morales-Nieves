# C2 - Trazabilidad end-to-end (Responsable: MORALES SANCHEZ GARY ALEJANDRO)

Esta carpeta reúne la trazabilidad end-to-end del ERS de MundiPets (43 elementos vigentes: 27 RF y 16 RNF), la línea base del proyecto y su sincronización con el product backlog.

## Contenido

- **`matriz_final/`** — Matriz de trazabilidad final completa: cadena Fuente → RF/RNF → CU → Clase UML → DFD → Estado → Criterio BDD → Caso de Prueba → Historia, más la columna de trazabilidad horizontal.
- **`huerfanos_cadenas_rotas/`** — Diagnóstico de cobertura: las 5 patologías detectadas (2 cadenas rotas, 3 trazas parciales) con su causa y la acción tomada para resolverlas. Cero requisitos huérfanos.
- **`sincronizacion_backlog/`** — Verificación de sincronización entre el product backlog (Jira) y el ERS, en ambas direcciones (RF → Historia e Historia → RF).
- **`capturas/`** — Evidencia visual: capturas del tablero Jira y de la matriz de trazabilidad, referenciadas desde el informe final.

## Resultado global

- 43 elementos evaluados, 100 % con fuente identificada.
- 0 requisitos huérfanos.
- 5 patologías detectadas en el diagrama de clases, las 5 resueltas.
- 100 % de sincronización entre el backlog y el ERS en ambas direcciones.
