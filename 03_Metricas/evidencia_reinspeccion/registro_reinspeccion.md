# Registro de la re-inspección (M6)

**Corresponde a:** Sección 5.3 y Anexo A.5 del informe · **Responsable:** Fuertes Arraes, Edson Daniel

## Qué se hizo

Para el cierre de la PE5 se re-inspeccionaron los 23 defectos originales del
subgrupo de Fuertes (informe de inspección Fagan de la PE4) sobre la versión
del ERS resultante del Change Control Board unificado (Sección 6.1),
verificando específicamente los tres requisitos que llegaron a RFC (RF-07,
RNF-03, RF-25) y una muestra de los 18 defectos corregidos directamente.

## Resultado: 0 de los 23 defectos originales permanece abierto

| Rango de defectos | Cantidad | Vía de cierre | Verificado en |
|---|---|---|---|
| D-01 a D-09, D-16 a D-20, D-22, D-23 | 18 | Corrección directa sobre el texto del ERS (sin RFC) | Sección 5.2 del informe |
| D-12 a D-15 | 4 | Corrección de la matriz de trazabilidad extendida | Coordinado con Morales Sánchez (Sección 6) |
| D-05, D-06 | (incluidos en RFC-01) | RFC-01, unificada como RFC-F: aplicada | Sección 6.1 (Morales Sánchez) |
| D-21, D-22 | (incluidos en RFC-02) | RFC-02, unificada como RFC-G: resuelta por vía alternativa | Sección 6.1 (Morales Sánchez) |
| D-10, D-11 | (incluidos en RFC-03) | RFC-03, unificada como RFC-A: ya correcta en el ERS vigente | Sección 6.1 (Morales Sánchez) |
| **Total defectos residuales** | **0 de 23** | | |

No se detectaron defectos nuevos introducidos por las correcciones aplicadas:
ninguna de las modificaciones revisadas contradice otro requisito, otra
sección del ERS o un modelo UML de la Sección 4.

## Hallazgos estructurales de plantilla (no computados como defectos Fagan)

La re-inspección identificó, aparte, dos hallazgos que **no** son defectos de
contenido (no se cuentan en el numerador de M6) sino ausencias de campo en el
propio formato de especificación:

1. Los 16 RNF no incluyen un campo explícito «Origen (ID de evidencia)» en su
   bloque de atributos, a diferencia de los 27 RF.
2. Las 9 RD no incluyen un campo explícito «Criterio de verificación» en su
   bloque de atributos: cuentan con «Justificación» e «Impacto», pero no con
   un criterio de aceptación comprobable homologado al de RF y RNF.

Ambos hallazgos alimentan la acción de mejora de **M1a** (ver
`../instrumento_auditoria/`), no la M6, y quedan coordinados con Gutiérrez
Ortega para la consolidación del ERS final (criterio C4).
