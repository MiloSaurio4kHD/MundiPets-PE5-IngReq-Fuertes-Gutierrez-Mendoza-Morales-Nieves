# Muestra de cinco requisitos para M5 (modificabilidad)

**Corresponde a:** Anexo A.4 del informe · **Responsable:** Fuertes Arraes, Edson Daniel

Muestra de cinco requisitos representativos, seleccionados por concentrar el
mayor número de enlaces cruzados verificables en el texto del ERS.

| Requisito | Descripción | Artefactos impactados si se modifica | Cantidad |
|---|---|---|---|
| RF-06 | Evaluar compatibilidad de cruza | RNF-06, RNF-07, RD-01, CU-06, CU-13 | 5 |
| RF-07 | Mensajería | RNF-15, CU-08 | 2 |
| RF-11 | Privacidad médica | RF-25, CU-12, RNF-16 | 3 |
| RF-25 | Aviso de extravío | RNF-16, RF-11, RD-04 | 3 |
| RNF-03 | Tiempo de respuesta | RNF-12, RF-04, RF-06, RF-17 | 4 |

```
M5 = (5 + 2 + 3 + 3 + 4) / 5 = 17 / 5 = 3,40
```

## Nota

RNF-03 es el requisito con mayor acoplamiento de la muestra (4 artefactos
impactados) y es precisamente el que motivó la RFC-02/RFC-G descrita en la
Sección 5.2 del informe: al modificar su umbral de rendimiento, el impacto se
propaga a otros tres requisitos (RNF-12, RF-04, RF-06, RF-17), lo que hace de
él un candidato natural para desacoplarse como restricción de infraestructura
independiente (ver acción de mejora de M5 en la Tabla de auditoría, Sección
8.3 del informe).
