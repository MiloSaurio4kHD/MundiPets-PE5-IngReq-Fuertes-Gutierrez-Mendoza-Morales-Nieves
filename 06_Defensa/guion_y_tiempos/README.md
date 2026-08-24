# Guion y distribución de tiempos de la defensa

## Datos generales

- **Proyecto:** MundiPets.
- **Fecha del ensayo:** 23 de agosto de 2026.
- **Modalidad:** Virtual.
- **Hora de inicio:** 15:00.
- **Hora de finalización:** 15:30.
- **Tiempo de exposición:** 20 minutos.
- **Tiempo para preguntas:** 10 minutos.
- **Duración total:** 30 minutos.
- **Coordinador:** Nieves Sánchez, Jimmy Samuel.

## Cronograma de exposición

| Intervalo | Tiempo | Diapositivas | Contenido | Responsable |
|---|---:|---:|---|---|
| 00:00-00:30 | 30 s | 1 | Portada y presentación del equipo | Nieves Sánchez |
| 00:30-03:00 | 2 min 30 s | 2 | Problema y contexto | Nieves Sánchez |
| 03:00-08:00 | 5 min | 3-5 | Stakeholders, proceso de ingeniería y ERS | Gutiérrez Ortega |
| 08:00-10:00 | 2 min | 6 | Modelos UML y trazabilidad | Morales Sánchez |
| 10:00-12:00 | 2 min | 7 | Resultados de la inspección | Fuertes Arraes |
| 12:00-16:00 | 4 min | 8 | Trazabilidad y métricas de calidad | Morales Sánchez y Fuertes Arraes |
| 16:00-19:00 | 3 min | 9 | Componentes de inteligencia artificial | Mendoza Párraga |
| 19:00-19:25 | 25 s | 10 | Lecciones aprendidas | Nieves Sánchez |
| 19:25-19:50 | 25 s | 11 | Conclusiones integradoras | Nieves Sánchez |
| 19:50-20:00 | 10 s | 12 | Cierre | Nieves Sánchez |
| 20:00-30:00 | 10 min | - | Preguntas del tribunal | Todo el equipo |

## Guion orientador

El siguiente texto funciona como guía. No debe leerse de manera literal durante la exposición.

### Diapositiva 1 - Portada

**Nieves Sánchez:**

> Buenos días. Somos el equipo responsable de MundiPets, una plataforma orientada a la adopción y cruza responsable de mascotas. En esta defensa presentaremos la integración del ERS, los resultados de la validación, las métricas de calidad y los componentes de inteligencia artificial.

### Diapositiva 2 - Problema y contexto

**Nieves Sánchez:**

> El problema identificado es que la información general y sanitaria de las mascotas se encuentra dispersa en diferentes medios, sin un canal centralizado y confiable. Esto facilita registros incompletos, falta de verificación y posibles estafas. MundiPets organiza esta información y considera las necesidades de propietarios, adoptantes, personas interesadas en cruza, refugios y veterinarias aliadas.

### Diapositivas 3 a 5 - Sistema, proceso y ERS

**Gutiérrez Ortega:**

> MundiPets considera cinco grupos principales de usuarios, cada uno con funciones y accesos diferentes. El proyecto evolucionó desde la comprensión del contexto en la PE1 hasta la integración y medición en la PE5. El ERS se organizó siguiendo la estructura de ISO/IEC/IEEE 29148:2018 y conserva la trazabilidad de los cambios aplicados a los requisitos principales.

### Diapositiva 6 - Modelos UML y trazabilidad

**Morales Sánchez:**

> La revisión comprobó que los requisitos aprobados estuvieran representados en los modelos UML. También se verificó el sentido inverso para confirmar que ningún elemento del modelo existiera sin un requisito que justificara su incorporación.

### Diapositiva 7 - Inspección

**Fuertes Arraes:**

> La inspección formal identificó 23 defectos: 2 críticos, 16 mayores y 5 menores. Después de las correcciones y la reinspección, ninguno de estos defectos permaneció abierto. Los hallazgos estructurales detectados posteriormente se registraron como acciones de mejora y no como defectos residuales.

### Diapositiva 8 - Trazabilidad y métricas

**Morales Sánchez y Fuertes Arraes:**

> Las métricas permitieron evaluar la calidad del ERS. M6 obtuvo 0,00 porque los defectos revisados fueron corregidos. M1a alcanzó 44,26 %, debido a que algunos RNF no incluyen el campo Origen y algunas restricciones de diseño no presentan un criterio de verificación explícito. El problema es estructural y no corresponde a contenido incorrecto.

### Diapositiva 9 - Componentes de inteligencia artificial

**Mendoza Párraga:**

> MundiPets incorpora tres componentes de inteligencia artificial: evaluación de compatibilidad para cruza, validación de imágenes de perfil y moderación de mensajes. Cada componente se relaciona con requisitos funcionales específicos y dispone de medidas alternativas cuando el servicio automático no está disponible.

### Diapositiva 10 - Lecciones aprendidas

**Nieves Sánchez:**

> Aprendimos que una inspección limitada a los requisitos escritos puede dejar fuera problemas de los modelos. La segunda auditoría encontró campos estructurales incompletos y confirmó que la trazabilidad debe revisarse más de una vez.

### Diapositiva 11 - Conclusiones

**Nieves Sánchez:**

> Concluimos que la elicitación, el ERS, los modelos UML, la validación, las métricas y la inteligencia artificial deben revisarse de manera integrada. Cada elemento del diseño necesita un requisito que lo respalde y una evidencia que permita verificarlo.

### Diapositiva 12 - Cierre

**Nieves Sánchez:**

> Muchas gracias por su atención. Estamos dispuestos a responder sus preguntas.

## Guion para las preguntas

Antes de responder, cada integrante deberá identificar el artefacto que contiene la evidencia:

- **ERS:** definición y criterio de verificación del requisito.
- **Matriz de trazabilidad:** origen, relaciones e impacto.
- **UML:** representación de las decisiones de diseño.
- **Informe de inspección:** defectos y correcciones.
- **Métricas:** resultados cuantitativos de calidad.
- **Anexos y Git:** evidencias, solicitudes de cambio y commits.

El equipo practicará con el [`banco de 22 preguntas`](../banco_preguntas/banco_22_preguntas.md). Cada integrante debe preparar al menos cuatro preguntas sobre bloques que no haya desarrollado directamente.

## Reglas de control del tiempo

1. Utilizar un temporizador visible desde el inicio.
2. Avisar discretamente cuando falten 30 segundos para terminar cada bloque.
3. No recuperar tiempo extendiendo el bloque siguiente.
4. Responder cada pregunta en un máximo aproximado de un minuto.
5. Si se desconoce un dato, reconocerlo y señalar el artefacto que debe revisarse.
