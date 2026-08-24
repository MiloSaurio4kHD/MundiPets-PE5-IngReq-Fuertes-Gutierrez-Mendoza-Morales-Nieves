# Análisis de pares de requisitos para M2 (consistencia)

**Corresponde a:** Anexo A.3 del informe · **Responsable:** Fuertes Arraes, Edson Daniel

| Par | Origen del análisis | Tipo de relación | Estado |
|---|---|---|---|
| RF-09 ↔ RD-03 | Defecto D-02 (inspección PE4) | Conflicto directo (validación/certificación) | Resuelto (Sección 5.2) |
| RF-07 ↔ RNF-15 | Defecto D-06 (inspección PE4) | Conflicto directo (moderación no especificada) | Resuelto (RFC-01/RFC-F) |
| RD-01 ↔ RNF-15 | Defecto D-07 (inspección PE4) | Conflicto directo (subcomponente de IA no declarado) | Resuelto (Sección 5.2) |
| RF-17 ↔ RNF-14 | Defecto D-08 (inspección PE4) | Conflicto directo (criterios de rechazo no enumerados) | Resuelto (Sección 5.2) |
| RF-25 ↔ RNF-16 | Defectos D-10/D-11 (inspección PE4) | Conflicto directo (exposición vs. protección de datos) | Resuelto (RFC-03/RFC-A) |
| RD-05 ↔ RNF-10 | Mención cruzada explícita en el texto del ERS | Relación declarada, sin conflicto | Sin acción |
| RD-08 ↔ RF-10 | Mención cruzada explícita en el texto del ERS | Relación declarada, sin conflicto | Sin acción |
| RD-08 ↔ RNF-09 | Mención cruzada explícita en el texto del ERS | Relación declarada, sin conflicto | Sin acción |
| RF-10 ↔ RNF-09 | Mención cruzada explícita en el texto del ERS | Relación declarada, sin conflicto | Sin acción |
| RNF-03 ↔ RNF-12 | Mención cruzada explícita en el texto del ERS | Relación declarada, sin conflicto | Sin acción |

## Metodología de búsqueda

Los **cinco pares con conflicto** provienen directamente del registro
consolidado de defectos de la inspección Fagan de la PE4 (Sección 5.1 del
informe), clasificados allí como tipo «Consistencia».

Los **cinco pares sin conflicto** se obtuvieron mediante revisión sistemática
de toda mención explícita de un identificador de requisito (RF-XX, RNF-XX o
RD-XX) dentro del texto de Descripción, Justificación o Impacto de cualquier
otro bloque de atributos del ERS, descartando las auto-referencias.

## Nota

RD-05 ↔ RD-08 ↔ RNF-09 comparten al menos un requisito con otro par de la
lista (RNF-09 aparece dos veces), lo cual es correcto: un mismo requisito
puede tener relación declarada con más de un requisito distinto sin que eso
cuente doble en el numerador de conflictos (solo se cuenta un conflicto si
hay contradicción real, no relación).
