# Plan de monitoreo en producción de los componentes de inteligencia artificial

| Componente | Indicador y frecuencia | Umbral de alerta por deriva | Criterio de reentrenamiento o retirada |
|---|---|---|---|
| **IA-01** | Coincidencia con evaluación veterinaria (RNF-IA-01), medida mensualmente sobre una muestra auditada de recomendaciones emitidas. | Caída sostenida por debajo de 80 % durante dos meses consecutivos. | Reentrenar con el conjunto de casos auditados del período; si tras el reentrenamiento no se recupera el umbral de RNF-06 en el siguiente ciclo, retirar el componente y volver al flujo manual declarado en su *fallback*. |
| **IA-02** | Tasa de clasificación correcta (RNF-IA-07), medida semanalmente sobre una muestra de imágenes revisadas manualmente como control de calidad. | Caída sostenida por debajo de 90 % durante tres semanas consecutivas. | Reentrenar incorporando los casos mal clasificados detectados en el control de calidad; si la tasa no se recupera en dos ciclos de reentrenamiento, derivar temporalmente todas las imágenes a revisión manual. |
| **IA-03** | Tasa de falsos bloqueos (RNF-IA-16, RNF-IA-17), medida mensualmente sobre una muestra de mensajes bloqueados revisados manualmente. | Tasa de falsos bloqueos superior a 15 % durante un mes de medición. | Reentrenar con los mensajes mal clasificados identificados en la revisión; si la tasa no mejora, desactivar temporalmente la moderación automática y operar con el canal de reporte manual entre usuarios. |

## Principio común

Ninguna deriva detectada retira un componente de forma automática. El umbral de alerta dispara una revisión y, si corresponde, un reentrenamiento; solo la falta de recuperación tras el reentrenamiento activa el *fallback* manual ya declarado en la ficha de cada componente, de modo que el sistema nunca queda sin una vía de operación cuando un componente de IA se degrada o deja de estar disponible.

## Trazado de los requisitos de IA

Los 27 requisitos de `../requisitos_RF_RNF/requisitos_IA.md` se trazan hacia los RF y RNF preexistentes del sistema:

- **IA-01** (RF-IA-01 a RF-IA-03, RNF-IA-01 a RNF-IA-06) → RF-06, RNF-06, RNF-13, RL-06.
- **IA-02** (RF-IA-07 a RF-IA-09, RNF-IA-07 a RNF-IA-12) → RF-17, RNF-07, RNF-14.
- **IA-03** (RF-IA-10 a RF-IA-12, RNF-IA-13 a RNF-IA-18) → RF-07, RNF-15.

Estas filas se entregan a Morales Sánchez para su integración en la matriz de trazabilidad final (Sección 6, Matriz de trazabilidad final): ningún requisito de IA queda aislado, porque todos sirven a una funcionalidad ya especificada o modifican su criterio de aceptación.
