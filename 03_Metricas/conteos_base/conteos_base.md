# Conteos base del ERS final de MundiPets

**Sección del informe:** Anexo A.2 · **Responsable:** Fuertes Arraes, Edson Daniel

Todos los conteos se obtuvieron contando sobre la versión del ERS efectivamente
entregada. Estos son los números que alimentan todas las fórmulas de
`../instrumento_auditoria/` y todos los cálculos de `../calculos/`.

| # | Conteo | Valor | Fuente en el ERS |
|---|---|---|---|
| 1 | Requisitos funcionales (RF) totales | 27 | Sección 3.2 (RF-01 a RF-27) |
| 2 | Requisitos no funcionales (RNF) totales | 16 | Sección 3.3 (RNF-01 a RNF-16) |
| 3 | Requisitos legales (RL) y de diseño (RD) | 9 + 9 = 18 | Sección 3.4 (RD-01 a RD-09) y 3.5 (RL-01 a RL-09) |
| 4 | Requisitos totales (RF+RNF+RD+RL) | 61 | — |
| 5 | Requisitos con los 4 atributos completos (ID, prioridad, fuente, criterio) | 27 | Solo RF; ver nota metodológica M1a en `../calculos/` |
| 6 | Casos de uso identificados | 13 | Sección 4.1, diagrama de casos de uso general |
| 7 | Casos de uso especificados textualmente | 13 | Sección 4.2 (CU-01 a CU-13) |
| 8 | Actores del sistema | 5 | Sección 4.1: Propietario de mascota, Adoptante, Interesado en cruza, Refugio de animales, Veterinaria |
| 9 | Actores con al menos un RF asociado | 5 | Los cinco actores del diagrama de casos de uso general tienen RF asociados explícitamente |
| 10 | Pares de requisitos analizados para consistencia | 10 | 5 con conflicto documentado en la inspección PE4 + 5 con relación cruzada explícita sin conflicto (ver `../calculos/analisis_pares_M2.md`) |
| 11 | Requisitos con criterio BDD comprobable (Gherkin) | 17 | Sección 4.5, matriz de trazabilidad extendida: filas que enlazan hasta HU con criterio de aceptación Gherkin |
| 12 | RF con cadena de trazabilidad hacia adelante completa | 17 | Igual fuente que el punto 11, expresado sobre el universo de 27 RF |
| 13 | RF con fuente o *stakeholder* identificado | 27 | Campo «Origen (ID de evidencia)» presente en el 100 % de los bloques de atributos de RF |
| 14 | Defectos hallados en la re-inspección de la PE5 | 0 | Ver `../evidencia_reinspeccion/`: los 23 defectos originales del registro consolidado de la PE4 quedaron cerrados |

## Regla

Si no se puede contar sobre el ERS con una referencia exacta de sección, no se
puede reportar. Cada fila de esta tabla debe poder verificarse abriendo el ERS
en la sección indicada.
