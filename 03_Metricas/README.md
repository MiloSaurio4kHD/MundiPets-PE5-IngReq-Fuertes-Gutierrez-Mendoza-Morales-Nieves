# 03_Metricas

Auditoría de calidad del ERS de MundiPets (Criterio C1, PE5). Contenido
correspondiente a la Sección 8 (Métricas de Calidad del ERS) y al Anexo A del
informe final. Responsable: FUERTES ARRAES, Edson Daniel.

## Contenido de cada subcarpeta

| Carpeta | Contenido | Corresponde a |
|---|---|---|
| `instrumento_auditoria/` | Las seis métricas, sus fórmulas, escala de valoración (0-4) y peso relativo | Sección 8.1 |
| `conteos_base/` | Los 14 conteos auditables sobre el ERS (RF, RNF, RD, RL, CU, actores, pares, etc.) con su fuente exacta | Anexo A.2 |
| `calculos/` | Las 6 métricas calculadas con aritmética completa (numerador/denominador visibles) y su nota de cálculo | Sección 8.2, Anexo A.3, Anexo A.4 |
| `evidencia_reinspeccion/` | Resultado de la re-inspección de la PE5 sobre los 23 defectos originales del subgrupo de Fuertes | Sección 5.3, Anexo A.5 |
| `antes_despues/` | Comparación antes/después de las métricas que mejoraron dentro del alcance de esta auditoría (M2, M6) | Sección 8.4 |

## Fuente de verdad

Los valores de este directorio deben coincidir siempre con la Sección 8 y el
Anexo A del `.tex` del informe final. Si se corrige un valor aquí, corregirlo
también allá (y viceversa) para que no haya inconsistencia entre el repositorio
y el documento entregado — la rúbrica de la PE5 lo penaliza explícitamente
(descuento DIA-S1).

## Nota pendiente de decisión del equipo

Al cierre de la Sección 6 (trazabilidad, Morales Sánchez) y la Sección 5.2
(correcciones, Fuertes Arraes), dos de las nueve mediciones podrían re-calcularse
con un valor más alto que el que aparece actualmente en `calculos/` y en la Tabla
de auditoría del informe:

- **M2 (consistencia):** actualmente 0,50 (contando los 5 conflictos como
  "detectados" sin importar que ya estén resueltos). Si se recalcula como
  conflictos **actualmente sin resolver** sobre los mismos 10 pares, el valor
  pasa a **1,00** (cumple el umbral ≥0,98).
- **M4ade (trazabilidad hacia adelante):** actualmente 62,96\,% (17/27 RF). Tras
  el cierre de cobertura de la Sección 6.3, los 27 RF ya tienen historia de
  usuario sincronizada, por lo que el valor real pasaría a **100,00\,%**.

Esto no se aplicó automáticamente porque implica editar tanto `calculos/` como
la Sección 8.3 y 8.4 del `.tex`, y esa decisión le corresponde al equipo. Si se
adopta, avisar a Gutiérrez Ortega para que quede reflejado también en la
consolidación del ERS.
