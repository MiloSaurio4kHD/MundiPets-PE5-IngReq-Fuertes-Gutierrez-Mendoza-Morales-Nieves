# Instrumento de auditoría de calidad del ERS

**Sección del informe:** 8.1 · **Responsable:** Fuertes Arraes, Edson Daniel

Se emplean las seis métricas fijadas por la guía de la PE5, cada una derivada
del modelo de calidad ISO/IEC 25010:2023 y de las características de
especificación de ISO/IEC/IEEE 29148:2018 (ver Fundamento Teórico, FT.1).

## Escala de valoración

| Valor | Significado |
|---|---|
| **4** | Cumple el valor de referencia con evidencia completa |
| **3** | Lo cumple con evidencia parcial |
| **2** | Queda por debajo del valor de referencia, pero con acción de mejora documentada |
| **1** | Queda por debajo sin acción |
| **0** | No se pudo medir |

## Peso relativo de cada métrica

| Métrica | Peso |
|---|---|
| M1 — Completitud | 0,20 |
| M2 — Consistencia | 0,15 |
| M3 — Verificabilidad | 0,20 |
| M4 — Trazabilidad | 0,20 |
| M5 — Modificabilidad | 0,10 |
| M6 — Corrección | 0,15 |

## Fórmulas

```
M1a  = req. con los 4 atributos completos / req. totales × 100
M1b  = CU especificados / CU identificados × 100
M1c  = actores con ≥ 1 RF / actores × 100

M2   = 1 − (conflictos detectados / pares de requisitos analizados)

M3   = req. con criterio BDD comprobable / req. totales × 100

M4ade = RF con cadena adelante completa / RF × 100
M4atr = RF con fuente o stakeholder identificado / RF × 100

M5   = (Σ req. afectados al modificar rᵢ, i = 1..5) / 5

M6   = defectos hallados después de la inspección / req. totales
```

## Valores de referencia (umbral de cumplimiento)

| Métrica | Umbral | Norma |
|---|---|---|
| M1a, M1b, M1c | ≥ 95 % | ISO 25010; ISO 29148 |
| M2 | ≥ 0,98 | ISO 25010 |
| M3 | ≥ 90 % | ISO 29148 |
| M4ade, M4atr | ≥ 90 % / = 100 % | ISO 29148 |
| M5 | ≤ 3,0 | ISO 25010 |
| M6 | ≤ 0,05 | ISO 25010 |

Los conteos base que alimentan cada fórmula están en `../conteos_base/`; el
cálculo completo de cada métrica está en `../calculos/`.
