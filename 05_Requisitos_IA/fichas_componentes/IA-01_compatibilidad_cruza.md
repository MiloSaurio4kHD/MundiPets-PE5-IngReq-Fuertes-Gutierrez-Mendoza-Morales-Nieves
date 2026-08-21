# Ficha del componente de inteligencia artificial IA-01

**Identificador y nombre:** IA-01 — Evaluación de compatibilidad para cruza

**Tarea y tipo:** Recomendación (*scoring* de compatibilidad con explicación causal)

**Entradas y salidas:**
- **Entrada:** raza, edad, sexo, estado de salud, antecedentes genéticos, parentesco e historial médico de las dos mascotas seleccionadas.
- **Salida:** nivel de compatibilidad (viable / riesgoso / requiere revisión veterinaria) junto con una explicación causal de máximo 60 palabras (RNF-13) y la advertencia de que el resultado es orientativo.

**Consumidor del resultado:** Propietario de mascota e interesado en cruza, para decidir si continúan o no con el proceso de cruza (RF-06); no autoriza ni rechaza el proceso de forma definitiva.

**Datos de entrenamiento:**
- *Origen:* historiales clínicos y genéticos registrados en la plataforma más evaluaciones veterinarias etiquetadas durante la fase de pruebas.
- *Volumen estimado:* conjunto inicial de al menos 300 pares de mascotas evaluados por veterinarios para el conjunto de referencia de RNF-06.
- *Etiquetado:* veterinario colegiado, sobre las mismas variables declaradas en RF-06.
- *Calidad mínima:* historiales con antecedentes genéticos y médicos completos; se descartan registros con campos obligatorios vacíos.
- *Sesgos conocidos:* sobrerrepresentación esperable de razas comunes en la zona de despliegue inicial frente a razas poco frecuentes, lo que puede degradar la exactitud en estas últimas.
- *Base legal:* consentimiento del titular y protección de datos desde el diseño (Art. 7, 8 y 39 LOPDP).
- *Conservación:* mientras la mascota o el propietario mantengan una cuenta activa en la plataforma.

**Métricas de éxito:**
- *Principal:* coincidencia con la evaluación veterinaria ≥ 85 % (RNF-06).
- *Secundarias:* tiempo de generación de la explicación ≤ 2 s y calificación media de comprensión ≥ 4/5 en escala Likert (RNF-13).
- *Conjunto de evaluación:* muestra representativa de pares de mascotas con evaluación veterinaria de referencia, distinta del conjunto de entrenamiento.

**Equidad:** Métrica: diferencia de tasa de coincidencia con la evaluación veterinaria entre razas comunes y razas poco representadas en los datos. Grupos comparados: razas con más de 30 casos en el conjunto de entrenamiento frente a razas con menos de 30 casos. Brecha máxima tolerada: 10 puntos porcentuales.

**Explicabilidad:** Se explica el resultado de compatibilidad al propietario y al interesado en cruza, en el momento de recibir el resultado, mediante una explicación causal por factores (raza, edad, estado de salud, antecedentes genéticos) de máximo 60 palabras, conforme a RNF-13 y al derecho a explicación de decisiones automatizadas de RL-06.

**Riesgos y *fallback*:** Si el modelo no está disponible o no alcanza el umbral mínimo de confianza en un caso concreto, el sistema muestra el mensaje "compatibilidad no determinada, se recomienda evaluación veterinaria" en lugar de forzar una recomendación; el proceso de cruza puede continuar manualmente sin el componente. Una recomendación errónea no bloquea la decisión final del usuario, que conserva la responsabilidad última.

**Clasificación de riesgo:** Riesgo limitado conforme al enfoque basado en riesgo del Reglamento (UE) 2024/1689: no es un sistema de identificación biométrica ni de puntuación social, pero al influir en una decisión con efecto sobre el bienestar animal exige las obligaciones de transparencia y explicabilidad ya declaradas en RNF-13 y RL-06.

**Plan de monitoreo:** Ver `plan_monitoreo/`. Indicador principal de coincidencia con evaluación veterinaria, medido mensualmente sobre una muestra de recomendaciones auditadas.

**Trazas:** RF-06, RNF-06, RNF-13, RD-01, RL-06.
