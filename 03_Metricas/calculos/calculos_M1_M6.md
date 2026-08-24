# Cálculo de las seis métricas con aritmética visible

**Sección del informe:** 8.2 · **Responsable:** Fuertes Arraes, Edson Daniel

Cada métrica muestra la división completa (numerador, denominador, resultado),
no solo el porcentaje final. Los números vienen de `../conteos_base/`.

---

## M1 — Completitud

```
M1a = req. con los 4 atributos completos / req. totales × 100
    = 27 / 61 × 100
    = 44,26 %

M1b = CU especificados / CU identificados × 100
    = 13 / 13 × 100
    = 100,00 %

M1c = actores con ≥ 1 RF / actores × 100
    = 5 / 5 × 100
    = 100,00 %
```

**Nota de cálculo — M1a.** El ERS emplea tres plantillas de atributos distintas
según el tipo de requisito. Los 27 RF son los únicos que declaran
explícitamente los cuatro atributos exigidos (identificador, prioridad
MoSCoW, fuente trazable mediante ID de evidencia, y criterio de verificación)
dentro de un único bloque. Los 16 RNF declaran identificador, prioridad y
criterio de verificación, pero no un campo de fuente empírica explícito (su
origen normativo es la característica ISO 25010 asociada, no una evidencia de
campo con ID propio). Las 9 RD declaran identificador, prioridad y
justificación (que funciona como fuente narrativa), pero no un criterio de
verificación explícito. Los 9 RL están estructurados como tabla de
trazabilidad legal (ID, artículo LOPDP, obligación, requisito que la
implementa) y no incluyen un campo de prioridad MoSCoW individual. Por tanto,
únicamente los 27 RF satisfacen los cuatro atributos en sentido estricto.

---

## M2 — Consistencia

```
M2 = 1 − (conflictos detectados / pares de requisitos analizados)
   = 1 − (5 / 10)
   = 0,50
```

**Nota de cálculo — M2.** Detalle completo de los 10 pares en
`analisis_pares_M2.md`. Resumen: 5 pares con conflicto documentado (idénticos
a los defectos de tipo Consistencia de la inspección Fagan de la PE4) + 5
pares con relación cruzada explícita sin conflicto. Los cinco conflictos son
de tipo **directo** (los dos requisitos se contradicen entre sí en el mismo
texto vigente); no se identificaron conflictos indirectos en esta muestra.
Los cinco conflictos ya quedaron resueltos (ver Sección 5.2 del informe); los
cinco pares sin conflicto no requieren acción.

---

## M3 — Verificabilidad

```
M3 = req. con criterio BDD comprobable / req. totales × 100
   = 17 / 61 × 100
   = 27,87 %
```

**Nota de cálculo — M3.** El dato de 17 proviene de la propia matriz de
trazabilidad extendida del ERS (Sección 4.5): de las 61 filas de
trazabilidad, 17 enlazan hasta una historia de usuario con su criterio de
aceptación en formato Gherkin (Dado/Cuando/Entonces) — específicamente, las
correspondientes a los RF de prioridad *Must* que cuentan con historia de
usuario especificada. El resto de los 61 requisitos —incluida la totalidad
de los 16 RNF, cuyo «Criterio de verificación» es una instrucción de prueba
en prosa y no un escenario Gherkin estructurado— no cuenta con este tipo de
criterio formal, aunque sí con un criterio de verificación textual de menor
formalidad. Se aplica aquí la definición **estricta** de «criterio BDD
comprobable» (formato Gherkin explícito), no la definición amplia de
«criterio de verificación textual».

---

## M4 — Trazabilidad

```
M4ade = RF con cadena adelante completa / RF × 100
      = 17 / 27 × 100
      = 62,96 %

M4atr = RF con fuente o stakeholder identificado / RF × 100
      = 27 / 27 × 100
      = 100,00 %
```

**Nota de cálculo — M4.** M4ade se calcula sobre el universo de 27 RF (no
sobre los 61 requisitos) porque la cadena hacia adelante
RF→CU→HU→Criterio de aceptación→Mockup es, por definición del propio modelo
de trazabilidad del ERS (Sección 4.5), una cadena que solo aplica a
requisitos funcionales orientados a caso de uso; los RNF, RD y RL no
participan de esa cadena por naturaleza. De los 27 RF, 17 tienen la cadena
completa hasta HU+CA (Gherkin); los 10 restantes son en su mayoría RF de
prioridad *Should* o *Could* sin historia de usuario dedicada. M4atr toma
como fuente el campo «Origen (ID de evidencia)», presente en el 100 % de
los RF.

---

## M5 — Modificabilidad

```
M5 = (Σ req. afectados al modificar rᵢ, i=1..5) / 5
   = (5 + 2 + 3 + 3 + 4) / 5
   = 17 / 5
   = 3,40
```

**Nota de cálculo — M5.** Detalle completo de la muestra en
`muestra_M5.md`. Resumen: muestra de cinco requisitos representativos,
seleccionados por concentrar el mayor número de enlaces cruzados verificables
en el texto del ERS: RF-06, RF-07, RF-11, RF-25 y RNF-03.

---

## M6 — Corrección

```
M6 = defectos hallados después de la inspección / req. totales
   = 0 / 61
   = 0,00
```

**Nota de cálculo — M6.** Numerador tomado directamente del resultado de la
re-inspección de la PE5 (ver `../evidencia_reinspeccion/`): de los 23
defectos originales, 0 permanece abierto sobre la versión del ERS resultante
del Change Control Board unificado. Los dos hallazgos estructurales de
plantilla identificados en la re-inspección (ausencia de campo «Origen» en
RNF y de campo «Criterio de verificación» en RD) se excluyen deliberadamente
de este numerador por no constituir defectos de contenido detectables
mediante el método Fagan, sino brechas de formato de plantilla; alimentan la
métrica M1, no la M6.
