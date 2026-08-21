# Datos de entrenamiento de los componentes de inteligencia artificial

Detalle ampliado del campo "Datos de entrenamiento" declarado en la ficha de cada componente (ver `../fichas_componentes/`).

## IA-01 — Evaluación de compatibilidad para cruza

| Campo | Detalle |
|---|---|
| Origen | Historiales clínicos y genéticos registrados en la plataforma más evaluaciones veterinarias etiquetadas durante la fase de pruebas. |
| Volumen estimado | Conjunto inicial de al menos 300 pares de mascotas evaluados por veterinarios para el conjunto de referencia de RNF-06. |
| Variables | Raza, edad, sexo, estado de salud, antecedentes genéticos, parentesco, historial médico. |
| Etiquetado | Veterinario colegiado, sobre las mismas variables declaradas en RF-06. |
| Calidad mínima | Historiales con antecedentes genéticos y médicos completos; se descartan registros con campos obligatorios vacíos. |
| Sesgos conocidos | Sobrerrepresentación esperable de razas comunes en la zona de despliegue inicial frente a razas poco frecuentes. |
| Base legal | Consentimiento del titular y protección de datos desde el diseño (Art. 7, 8 y 39 LOPDP; Reglamento General LOPDP). |
| Conservación | Mientras la mascota o el propietario mantengan una cuenta activa en la plataforma. |

## IA-02 — Validación de imágenes de perfil

| Campo | Detalle |
|---|---|
| Origen | Conjunto etiquetado de fotografías de mascotas (válidas) y de imágenes irrelevantes, ofensivas o de baja calidad (inválidas). |
| Volumen estimado | Conjunto de evaluación con representación equilibrada de ambas clases, suficiente para sostener la meta de RNF-07. |
| Variables | Imagen cargada al perfil de la mascota. |
| Etiquetado | Manual, por el equipo responsable de moderación de contenido, según la política de contenido de la plataforma. |
| Calidad mínima | Imágenes con resolución legible; se descartan archivos corruptos o no soportados antes del etiquetado. |
| Sesgos conocidos | Posible menor exactitud en especies poco representadas en el conjunto inicial (distintas a perros y gatos). |
| Base legal | Consentimiento del titular al publicar contenido e interés legítimo de la plataforma (Art. 7 y 8 LOPDP). |
| Conservación | Mientras la publicación permanezca activa en la plataforma. |

## IA-03 — Moderación de mensajes

| Campo | Detalle |
|---|---|
| Origen | Conjunto etiquetado de mensajes de ejemplo con y sin contenido inapropiado. |
| Volumen estimado | Conjunto de evaluación balanceado entre las categorías declaradas (ofensivo, spam, pago externo, fuera de tema, apropiado). |
| Variables | Texto del mensaje enviado entre dos usuarios. |
| Etiquetado | Manual, por el equipo de moderación, según la política de contenido de mensajería. |
| Calidad mínima | Mensajes en español, del dominio de adopción/cruza de mascotas, sin datos personales de terceros no involucrados. |
| Sesgos conocidos | Riesgo de sobre-bloqueo de mensajes con vocabulario coloquial del dominio veterinario no visto en entrenamiento. |
| Base legal | Interés legítimo de la plataforma y consentimiento del titular al aceptar los términos de uso (Art. 7, 8 y 10 lit. e LOPDP). |
| Conservación | Mientras ambos usuarios mantengan cuenta activa; los mensajes bloqueados no se entregan pero se registran para auditoría. |
