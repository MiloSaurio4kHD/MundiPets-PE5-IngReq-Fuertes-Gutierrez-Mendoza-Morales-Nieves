# Sincronización entre el product backlog y el ERS

**Herramienta de tablero declarada:** Jira (proyecto Kanban "MundiPets", clave `KAN`), con 5 Épicas, 27 Historias y 25 Subtareas.

## Verificación de sincronización

| Verificación | Total | Cumple | % |
|---|---|---|---|
| RF con al menos una historia de usuario asociada | 27 | 27 | **100 %** |
| Historias del backlog con un RF de origen identificado | 27 | 27 | **100 %** |

## Metodología de verificación

La verificación se realizó en ambas direcciones, conforme exige la guía:

- **Dirección RF → Historia:** los 27 RF de prioridad Must, Should y Could del ERS (RF-01 a RF-27) tienen exactamente una tarjeta en Jira que los referencia explícitamente en el campo "RF asociado". Ningún RF quedó sin cobertura y ninguno tiene más de una historia duplicada.
- **Dirección Historia → RF:** las 27 tarjetas de tipo Historia apuntan cada una a un RF real y existente en el ERS, sin tarjetas huérfanas del lado del backlog.

Cada tarjeta incluye además, en su descripción, el número de HU (coincide con las 27 historias HU-01 a HU-27 redactadas para este informe), la prioridad MoSCoW y la fuente de evidencia, replicando fielmente el contenido del ERS dentro del tablero.

## Diagnóstico

Sincronización del **100 %** en ambas direcciones. No se detectaron RF sin historia, historias sin RF de origen, ni duplicados.

Este resultado es consistente con haber completado las 12 historias faltantes (HU-16 a HU-27) antes de construir el tablero, lo que evitó que Jira heredara el vacío de cobertura que existía inicialmente solo en el documento del ERS.
