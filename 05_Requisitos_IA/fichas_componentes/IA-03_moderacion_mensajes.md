# Ficha del componente de inteligencia artificial IA-03

**Identificador y nombre:** IA-03 — Moderación de mensajes

**Tarea y tipo:** Clasificación (texto: lenguaje ofensivo / spam / solicitud de pago externo / conversación dentro de tema)

**Entradas y salidas:**
- **Entrada:** texto del mensaje enviado entre dos usuarios en el sistema de mensajería (RF-07).
- **Salida:** decisión de entrega o bloqueo del mensaje y, si se bloquea, la categoría de infracción detectada (RNF-15) mostrada antes del bloqueo.

**Consumidor del resultado:** El usuario que redacta el mensaje, que recibe la notificación de bloqueo con la categoría antes de que el mensaje se envíe.

**Datos de entrenamiento:**
- *Origen:* conjunto etiquetado de mensajes de ejemplo con y sin contenido inapropiado, construido para las pruebas del componente.
- *Volumen estimado:* conjunto de evaluación balanceado entre las categorías declaradas (ofensivo, spam, pago externo, fuera de tema, apropiado).
- *Etiquetado:* manual, por el equipo de moderación, según la política de contenido de mensajería.
- *Calidad mínima:* mensajes en español, del dominio de adopción/cruza de mascotas, sin datos personales de terceros no involucrados.
- *Sesgos conocidos:* riesgo de sobre-bloqueo de mensajes con vocabulario coloquial del dominio veterinario que el modelo no ha visto en entrenamiento (por ejemplo, términos médicos poco comunes mal clasificados como spam).
- *Base legal:* interés legítimo de la plataforma en prevenir fraude y contenido ofensivo, y consentimiento del titular al aceptar los términos de uso de la mensajería (Art. 7, 8 y 10 lit. e LOPDP).
- *Conservación:* la conversación se conserva mientras ambos usuarios mantengan cuenta activa; los mensajes bloqueados no se entregan pero se registran para auditoría de moderación.

**Métricas de éxito:**
- *Principal:* 100 % de los mensajes moderados con categoría de infracción mostrada antes del bloqueo (RNF-15).
- *Secundaria:* calificación media de comprensión de la notificación ≥ 4/5 (RNF-15).
- *Conjunto de evaluación:* lote de mensajes de prueba etiquetados manualmente, con casos de las cuatro categorías de infracción y de mensajes apropiados.

**Equidad:** Métrica: diferencia de tasa de falsos bloqueos (mensajes apropiados marcados como infracción) entre mensajes que usan vocabulario técnico veterinario y mensajes de lenguaje general. Grupos comparados: mensajes con terminología clínica frente a mensajes sin ella. Brecha máxima tolerada: 10 puntos porcentuales.

**Explicabilidad:** Se explica al remitente, antes de bloquear el envío, la categoría de infracción detectada mediante una explicación por ejemplos ("mensajes como este suelen clasificarse como X"), conforme a RNF-15.

**Riesgos y *fallback*:** Si el componente no está disponible, los mensajes se entregan sin moderación automática y quedan sujetos al canal de reporte manual entre usuarios, en vez de bloquear por completo la mensajería. Un falso bloqueo puede apelarse solicitando revisión manual del mensaje retenido.

**Clasificación de riesgo:** Riesgo limitado conforme al Reglamento (UE) 2024/1689: modera comunicación entre usuarios sin tomar decisiones sobre acceso a servicios esenciales; su obligación principal es la transparencia de la categoría de bloqueo, ya cubierta por RNF-15.

**Plan de monitoreo:** Ver `plan_monitoreo/`. Indicador de tasa de falsos bloqueos, medido mensualmente sobre una muestra de mensajes bloqueados revisados manualmente.

**Trazas:** RF-07, RNF-15, RD-01.
