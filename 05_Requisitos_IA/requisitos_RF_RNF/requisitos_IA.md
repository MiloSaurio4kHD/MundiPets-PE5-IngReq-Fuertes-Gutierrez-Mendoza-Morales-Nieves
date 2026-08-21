# Requisitos funcionales y no funcionales de los componentes de IA

27 requisitos (9 por componente: 3 RF + 3 RNF de rendimiento + 2 RNF de equidad + 1 RNF de explicabilidad).

## IA-01 — Evaluación de compatibilidad para cruza

| ID | Tipo | Enunciado con umbral y unidad | Método de comprobación |
|---|---|---|---|
| RF-IA-01 | RF | El sistema deberá generar un resultado de compatibilidad (viable / riesgoso / requiere revisión veterinaria) para todo par de mascotas seleccionado, en un tiempo máximo de 3 s. | Seleccionar 20 pares de mascotas y medir el tiempo hasta obtener el resultado. |
| RF-IA-02 | RF | El sistema deberá mostrar, junto al resultado de compatibilidad, una explicación causal de máximo 60 palabras que liste los factores considerados (raza, edad, estado de salud, antecedentes genéticos). | Verificar en 20 casos de prueba que la explicación no supere 60 palabras y mencione al menos dos factores. |
| RF-IA-03 | RF | El sistema deberá incluir la advertencia "resultado orientativo, no sustituye evaluación veterinaria" en el 100 % de los resultados de compatibilidad emitidos. | Revisar 20 resultados emitidos y comprobar la presencia literal de la advertencia. |
| RNF-IA-01 | Rendimiento | El sistema deberá generar recomendaciones de compatibilidad con una coincidencia ≥ 85 % respecto a la evaluación veterinaria de referencia (RNF-06). | Comparar 100 recomendaciones contra la evaluación de un veterinario sobre el conjunto de prueba. |
| RNF-IA-02 | Rendimiento | El sistema deberá generar la explicación causal en un tiempo no mayor a 2 s (RNF-13). | Medir el tiempo de generación en 30 solicitudes consecutivas. |
| RNF-IA-03 | Rendimiento | El sistema deberá mantener el componente de compatibilidad disponible ≥ 99 % del tiempo mensual, mostrando un mensaje de no disponibilidad ante fallas en lugar de bloquear el flujo de cruza. | Registrar el tiempo de actividad del servicio de IA durante un mes de monitoreo. |
| RNF-IA-04 | Equidad | El sistema deberá mantener una diferencia de tasa de coincidencia con la evaluación veterinaria no mayor a 10 puntos porcentuales entre razas con >30 casos y razas con <30 casos en el conjunto de entrenamiento. | Calcular la tasa de coincidencia por grupo de razas sobre el conjunto de evaluación y comparar la brecha. |
| RNF-IA-05 | Equidad | El sistema deberá mantener una diferencia de tasa de coincidencia no mayor a 10 puntos porcentuales entre mascotas de razas puras y mestizas. | Calcular la tasa de coincidencia por subgrupo (pura / mestiza) sobre el conjunto de evaluación y comparar la brecha. |
| RNF-IA-06 | Explicabilidad | El sistema deberá lograr una calificación media de comprensión de la explicación ≥ 4/5 en escala Likert 1–5 (RNF-13). | Aplicar encuesta de comprensión a usuarios técnicos y no técnicos tras mostrar el resultado. |

## IA-02 — Validación de imágenes de perfil

| ID | Tipo | Enunciado con umbral y unidad | Método de comprobación |
|---|---|---|---|
| RF-IA-07 | RF | El sistema deberá clasificar toda imagen cargada como aceptada o rechazada en un tiempo máximo de 2 s. | Cargar 30 imágenes y medir el tiempo de respuesta de la clasificación. |
| RF-IA-08 | RF | El sistema deberá mostrar, cuando una imagen sea rechazada, el motivo específico del rechazo en máximo 30 palabras (RNF-14). | Cargar 15 imágenes inválidas y verificar la presencia y extensión del motivo mostrado. |
| RF-IA-09 | RF | El sistema deberá permitir cargar una nueva imagen de forma inmediata tras un rechazo, sin reiniciar el flujo de publicación. | Rechazar una imagen y comprobar que el usuario puede cargar una nueva sin salir del formulario de publicación. |
| RNF-IA-07 | Rendimiento | El sistema deberá clasificar correctamente ≥ 95 % de las imágenes del conjunto de evaluación (RNF-07). | Evaluar el componente contra un conjunto de imágenes etiquetadas manualmente y calcular la tasa de acierto. |
| RNF-IA-08 | Rendimiento | El sistema deberá procesar imágenes de hasta 10 MB sin superar el tiempo de clasificación declarado en RF-IA-07. | Cargar imágenes de distintos tamaños (hasta 10 MB) y medir el tiempo de clasificación. |
| RNF-IA-09 | Rendimiento | El sistema deberá mantener el componente de validación disponible ≥ 99 % del tiempo mensual, derivando la imagen a revisión manual en caso de indisponibilidad en lugar de bloquear la publicación. | Registrar el tiempo de actividad del servicio de validación de imágenes durante un mes de monitoreo. |
| RNF-IA-10 | Equidad | El sistema deberá mantener una diferencia de tasa de clasificación correcta no mayor a 10 puntos porcentuales entre especies con >50 imágenes de referencia y especies con <50. | Calcular la tasa de acierto por especie sobre el conjunto de evaluación y comparar la brecha. |
| RNF-IA-11 | Equidad | El sistema deberá mantener una diferencia de tasa de falso rechazo no mayor a 10 puntos porcentuales entre imágenes con buena y baja iluminación. | Evaluar el componente sobre subconjuntos de imágenes agrupados por condición de iluminación. |
| RNF-IA-12 | Explicabilidad | El sistema deberá mostrar un motivo específico en el 100 % de los rechazos, con calificación media de comprensión ≥ 4/5 en escala Likert. | Revisar 15 rechazos y encuestar la comprensión del motivo mostrado a los usuarios. |

## IA-03 — Moderación de mensajes

| ID | Tipo | Enunciado con umbral y unidad | Método de comprobación |
|---|---|---|---|
| RF-IA-10 | RF | El sistema deberá clasificar todo mensaje enviado como apropiado o infractor (ofensivo, spam, pago externo, fuera de tema) antes de su entrega. | Enviar 30 mensajes de las cuatro categorías de infracción y uno apropiado, y verificar la clasificación. |
| RF-IA-11 | RF | El sistema deberá mostrar, cuando un mensaje sea bloqueado, la categoría de infracción detectada antes de impedir el envío (RNF-15). | Enviar 15 mensajes con contenido inapropiado y verificar que se muestra la categoría antes del bloqueo. |
| RF-IA-12 | RF | El sistema deberá permitir editar y reenviar un mensaje bloqueado sin perder el contenido no infractor del mensaje original. | Bloquear un mensaje, editarlo y comprobar que el sistema conserva el texto no infractor al reenviarlo. |
| RNF-IA-13 | Rendimiento | El sistema deberá emitir la decisión de moderación en un tiempo máximo de 1 s desde el envío del mensaje. | Enviar 30 mensajes y medir el tiempo entre el envío y la decisión de moderación. |
| RNF-IA-14 | Rendimiento | El sistema deberá mostrar la categoría de infracción en el 100 % de los mensajes moderados, antes del bloqueo (RNF-15). | Revisar 15 mensajes bloqueados y comprobar la presencia de la categoría mostrada. |
| RNF-IA-15 | Rendimiento | El sistema deberá mantener el componente de moderación disponible ≥ 99 % del tiempo mensual, entregando los mensajes sin moderación automática en caso de indisponibilidad en lugar de bloquear la mensajería. | Registrar el tiempo de actividad del servicio de moderación durante un mes de monitoreo. |
| RNF-IA-16 | Equidad | El sistema deberá mantener una diferencia de tasa de falso bloqueo no mayor a 10 puntos porcentuales entre mensajes con vocabulario técnico veterinario y mensajes de lenguaje general. | Evaluar el componente sobre subconjuntos de mensajes agrupados por tipo de vocabulario y comparar la brecha. |
| RNF-IA-17 | Equidad | El sistema deberá mantener una diferencia de tasa de falso bloqueo no mayor a 10 puntos porcentuales entre mensajes largos (>200 caracteres) y mensajes cortos. | Evaluar el componente sobre subconjuntos de mensajes agrupados por longitud y comparar la brecha. |
| RNF-IA-18 | Explicabilidad | El sistema deberá lograr una calificación media de comprensión de la notificación de bloqueo ≥ 4/5 en escala Likert 1–5. | Aplicar encuesta de comprensión a usuarios tras recibir una notificación de bloqueo. |

## Trazas hacia el ERS

- **IA-01** (RF-IA-01 a RF-IA-03, RNF-IA-01 a RNF-IA-06) → RF-06, RNF-06, RNF-13, RL-06.
- **IA-02** (RF-IA-07 a RF-IA-09, RNF-IA-07 a RNF-IA-12) → RF-17, RNF-07, RNF-14.
- **IA-03** (RF-IA-10 a RF-IA-12, RNF-IA-13 a RNF-IA-18) → RF-07, RNF-15.

Estas filas se entregan a Morales Sánchez para su integración en la matriz de trazabilidad final.
