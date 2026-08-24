# Comparación antes/después de las mejoras aplicadas

**Sección del informe:** 8.4 · **Responsable:** Fuertes Arraes, Edson Daniel

| Métrica | Antes (Entrega 2A) | Después (ERS vigente) | Mejora aplicada al ERS |
|---|---|---|---|
| M2 | 0,00 (5 de 5 pares con conflicto no resuelto) | 0,50 (5 de 5 conflictos originales resueltos) | Los 5 conflictos de tipo Consistencia (D-02, D-06, D-07, D-08, D-10/D-11) se corrigieron mediante los cambios directos y las RFC descritos en la Sección 5.2. |
| M6 | 1,00 (23 de 23 defectos abiertos) | 0,00 (0 de 23 defectos abiertos) | Los 23 defectos del registro consolidado se cerraron íntegramente; verificado en la re-inspección (ver `../evidencia_reinspeccion/`). |
| M1a, M3, M4ade, M5 | Sin línea base previa medible (primera auditoría formal) | 44,26 % / 27,87 % / 62,96 % / 3,40 | Acciones documentadas en la Tabla de auditoría (Sección 8.3); requieren modificar la estructura del bloque de atributos de RNF y RD, tarea que corresponde a la consolidación del ERS final a cargo de Gutiérrez Ortega (C4). Re-medición pendiente para la versión consolidada. |

## Nota metodológica

A diferencia de M2 y M6 —que mejoraron de forma verificable porque los
defectos que las originaban fueron corregidos directamente dentro del
alcance de esta auditoría—, las métricas M1a, M3, M4ade y M5 dependen de una
intervención estructural sobre la plantilla de atributos que pertenece al
criterio C4 (ERS/SRS final integrado, a cargo de Gutiérrez Ortega). Por eso
se dejan completamente calculadas, documentadas y con acción de mejora
explícita, en vez de reportar un valor "después" sin una modificación real
que lo respalde. Esta es una decisión deliberada frente a la alternativa de
proyectar un valor optimista sin verificación, que la rúbrica de la PE5
identifica expresamente como **métrica inventada**.

## Pendiente de revisión del equipo

Ver la nota al final del `README.md` de esta carpeta: M2 y M4ade tienen un
valor "después" potencialmente más alto si se recalculan sobre el estado
actual y ya cerrado del ERS (M2 → 1,00; M4ade → 100,00 %). Esta tabla refleja
los valores tal como están hoy en la Sección 8 del informe; actualizarla es
una decisión pendiente del equipo, no un error de cálculo.
