# Ficha del componente de inteligencia artificial IA-02

**Identificador y nombre:** IA-02 — Validación de imágenes de perfil

**Tarea y tipo:** Clasificación (visión: imagen válida / inválida, con motivo de rechazo)

**Entradas y salidas:**
- **Entrada:** imagen cargada por el usuario al perfil de una mascota.
- **Salida:** resultado binario (aceptada / rechazada) y, si es rechazada, el motivo específico (contenido inapropiado, imagen borrosa, tipo de fotografía incorrecto) en máximo 30 palabras (RNF-14).

**Consumidor del resultado:** Propietario de mascota, que recibe el resultado al momento de publicar; veterinaria, en el caso de imágenes asociadas a validación de información médica.

**Datos de entrenamiento:**
- *Origen:* conjunto etiquetado de fotografías de mascotas (válidas) y de imágenes irrelevantes, ofensivas o de baja calidad (inválidas), construido para las pruebas de RNF-07.
- *Volumen estimado:* conjunto de evaluación con representación equilibrada de ambas clases, suficiente para sostener la meta de RNF-07.
- *Etiquetado:* manual, por el equipo responsable de moderación de contenido, siguiendo la política de contenido de la plataforma.
- *Calidad mínima:* imágenes con resolución legible; se descartan archivos corruptos o no soportados antes del etiquetado.
- *Sesgos conocidos:* posible menor exactitud en mascotas de especies poco representadas en el conjunto inicial (por ejemplo, especies distintas a perros y gatos).
- *Base legal:* consentimiento del titular al publicar contenido e interés legítimo de la plataforma en mantener la política de contenido (Art. 7 y 8 LOPDP).
- *Conservación:* mientras la publicación permanezca activa en la plataforma.

**Métricas de éxito:**
- *Principal:* clasificación correcta ≥ 95 % (RNF-07).
- *Secundaria:* 100 % de los rechazos con motivo específico mostrado y calificación media de comprensión ≥ 4/5 (RNF-14).
- *Conjunto de evaluación:* lote de imágenes etiquetadas manualmente, distinto del usado para ajustar el clasificador.

**Equidad:** Métrica: diferencia de tasa de rechazo correcto entre especies con mayor representación en el conjunto de entrenamiento (perros, gatos) y especies con menor representación. Grupos comparados: especies con más de 50 imágenes de referencia frente a especies con menos de 50. Brecha máxima tolerada: 10 puntos porcentuales.

**Explicabilidad:** Se explica el motivo del rechazo al propietario, en el momento de intentar publicar la imagen, mediante una explicación por contraste ("se rechazó por X en lugar de Y") de máximo 30 palabras, conforme a RNF-14.

**Riesgos y *fallback*:** Si el componente no está disponible, el sistema permite la publicación en estado "pendiente de revisión" y la deriva a moderación manual, en vez de bloquear indefinidamente al usuario. Un falso rechazo puede apelarse mediante revisión manual; un falso positivo (imagen inapropiada no detectada) queda sujeto al reporte posterior de otros usuarios.

**Clasificación de riesgo:** Riesgo mínimo/limitado conforme al Reglamento (UE) 2024/1689: es un sistema de moderación de contenido, no de identificación de personas; su principal obligación derivada es la transparencia del motivo de rechazo, ya cubierta por RNF-14.

**Plan de monitoreo:** Ver `plan_monitoreo/`. Indicador de tasa de clasificación correcta, medido sobre una muestra semanal de imágenes revisadas manualmente como control de calidad.

**Trazas:** RF-17, RNF-07, RNF-14, RD-01.
