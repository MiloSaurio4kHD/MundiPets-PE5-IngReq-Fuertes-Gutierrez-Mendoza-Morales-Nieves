# Banco de 22 preguntas del tribunal, respuesta preparada y artefacto de respaldo

## Fundamentos

**1. ¿Cuál es la frontera del sistema y qué queda deliberadamente fuera?**
El límite comprende gestión de perfiles, publicación de anuncios, búsqueda y comunicación entre usuarios, y registro de información sanitaria validada. Quedan fuera la atención veterinaria en sí misma, el transporte de mascotas y la gestión legal de tenencia.
*Artefacto: ERS; diagrama de contexto.*

**2. ¿Por qué se siguió el proceso de PE1 a PE5 y no se especificó todo de una vez?**
Porque los requisitos de MundiPets, especialmente los que dependen de evidencia de campo (entrevistas, cuestionario, walkthroughs) y de los componentes de IA, no podían fijarse sin validar primero con los usuarios reales; el proceso iterativo permitió detectar defectos en la PE4 y corregirlos antes de esta entrega.
*Artefacto: ERS; historial de versiones del ERS.*

## Elicitación

**3. ¿Qué técnicas de elicitación usó el equipo y por qué esas y no otras?**
Entrevista semiestructurada como técnica principal (EV-01 a EV-18, EV-23 y EV-24), complementada con un cuestionario (61 respuestas válidas) y con sesiones de validación *walkthrough* grabadas en video con consentimiento (EV-19 a EV-24), sobre usuarios técnicos (veterinarias) y no técnicos (propietarios). Se prefirió esta combinación sobre una encuesta única porque el dominio requiere profundidad sobre procesos poco formalizados que el cuestionario por sí solo no captura.
*Artefacto: ERS; cuestionario; evidencia EV-01 a EV-24.*

**4. Muéstrenme un requisito que nació de una entrevista con una veterinaria.**
RF-26 y RF-27 nacieron directamente de la evidencia EV-23 (walkthrough/entrevista con PROP-12) y EV-24 (walkthrough/entrevista con VET-07) recolectada específicamente para esta entrega.
*Artefacto: ERS; evidencia EV-23/EV-24; historial de versiones del ERS (v4.0).*

## Especificación

**5. ¿Cómo se estructura el ERS conforme a la norma que citan?**
El ERS sigue la estructura de cláusulas de contenido de ISO/IEC/IEEE 29148:2018, con correspondencia explícita entre cada cláusula de la norma y la sección del documento del equipo.
*Artefacto: ERS.*

**6. Muéstrenme un requisito y díganme de qué evidencia concreta nació.**
RF-06 (evaluar compatibilidad para cruza) tiene como origen la evidencia EV-01 a EV-08, EV-11, EV-13 a EV-16: los propietarios e interesados en cruza entrevistados señalaron reiteradamente la dificultad de evaluar de forma informal la compatibilidad entre mascotas.
*Artefacto: ERS, ficha de RF-06 (campo "Origen ID de evidencia").*

**7. ¿Cómo se aplicó MoSCoW y por qué también Kano y WSJF?**
MoSCoW clasificó los requisitos por urgencia de implementación (Must/Should/Could/Won't); Kano se usó para distinguir funcionalidades básicas de las que generan satisfacción diferencial, con base en las respuestas del cuestionario; WSJF ordenó el trabajo por relación entre costo del retraso y tamaño del esfuerzo, mostrando que el valor más alto no siempre encabeza la lista de prioridad.
*Artefacto: ERS; cuestionario; tablas de priorización MoSCoW, Kano y WSJF.*

## Validación

**8. ¿Qué defectos se encontraron en la inspección de la PE4 y cómo se corrigieron?**
*(Completar con el resumen de defectos de la inspección de la PE4 y las correcciones aplicadas — responsable: Fuertes.)*
*Artefacto: informe de inspección de la PE4.*

**9. ¿Qué defectos residuales quedaron tras la re-inspección de la PE5?**
*(Completar con el registro de defectos residuales de la re-inspección — responsable: Fuertes.)*
*Artefacto: registro de re-inspección; Anexo A.*

**10. ¿Cómo se valida un requisito con criterio BDD?**
Cada requisito con criterio BDD comprobable se redacta en formato Dado/Cuando/Entonces y se verifica ejecutando el escenario descrito contra el comportamiento observado del sistema o del MVP.
*Artefacto: ERS; Tabla 3, conteo #11 (requisitos con criterio BDD comprobable).*

## Gestión

**11. ¿Cómo se controla la versión del ERS y se evita un identificador duplicado?**
El ERS final declara número de versión, fecha de congelación, hash de commit y etiqueta de línea base en Git; se verifica unicidad de identificadores en las series RF, RNF, RL, RD, CU y RF-IA antes de cerrar la entrega.
*Artefacto: ERS; repositorio Git (etiqueta de línea base).*

**12. Muéstrenme un requisito nuevo incorporado en esta entrega y díganme por qué.**
RF-26 y RF-27, incorporados en la versión 4.0 del ERS a partir de la evidencia EV-23 y EV-24 recolectada para esta entrega, tras la inspección de la PE4.
*Artefacto: ERS, historial de versiones (v4.0).*

**13. Tomen un RF y díganme qué se rompería si mañana cambia.**
Si RF-06 (evaluar compatibilidad para cruza) cambiara, se rompería su explicabilidad legal asociada (RNF-13, exigida por RL-06, Art. 20 LOPDP), su métrica de exactitud (RNF-06) y los 9 requisitos de IA-01 que trazan hacia él.
*Artefacto: ERS, fichas RF-06/RNF-06/RNF-13/RL-06; tabla de requisitos de IA; matriz de trazabilidad final.*

## Inteligencia artificial

**14. ¿Qué componentes de IA tiene MundiPets y por qué esos y no otros?**
Tres: evaluación de compatibilidad para cruza (IA-01), validación de imágenes de perfil (IA-02) y moderación de mensajes (IA-03), cada uno justificado con evidencia documental propia (EV-01 a EV-08, EV-11, EV-13 a EV-16 para IA-01; EV-01, EV-03, EV-05, EV-07, EV-08 para IA-02; EV-02, EV-07, EV-08 para IA-03), no por moda tecnológica.
*Artefacto: fichas de componentes de IA.*

**15. ¿Qué pasa si un componente de IA no está disponible?**
Ninguno bloquea el sistema: IA-01 muestra "compatibilidad no determinada, se recomienda evaluación veterinaria"; IA-02 deriva la imagen a revisión manual; IA-03 entrega los mensajes sin moderación automática. Los tres mantienen ≥ 99 % de disponibilidad mensual como objetivo.
*Artefacto: fichas de IA-01, IA-02, IA-03 (campo "Riesgos y *fallback*"); plan de monitoreo.*

**16. ¿Qué decide el modelo y qué pasa cuando se equivoca?**
IA-01 decide un nivel de compatibilidad orientativo, nunca definitivo; IA-02 decide aceptar o rechazar una imagen, con posibilidad de apelación por revisión manual; IA-03 decide bloquear o entregar un mensaje, también apelable. Ningún error de los tres componentes toma la decisión final por el usuario.
*Artefacto: fichas de IA-01, IA-02, IA-03 (campos "Consumidor del resultado" y "Riesgos y *fallback*").*

**17. ¿Cómo se mide la equidad de los componentes de IA y qué brecha se tolera?**
Cada componente mide la diferencia de tasa de acierto (o falso bloqueo/rechazo) entre subgrupos con distinta representación en los datos —razas, especies e iluminación, o tipo de vocabulario y longitud del mensaje— con una brecha máxima tolerada de 10 puntos porcentuales en los 6 RNF de equidad.
*Artefacto: tabla de requisitos de IA (RNF-IA-04, RNF-IA-05, RNF-IA-10, RNF-IA-11, RNF-IA-16, RNF-IA-17).*

**18. ¿Cuál es la base legal para tratar los datos que usan los componentes de IA?**
El consentimiento del titular y la protección de datos desde el diseño conforme a los Art. 7, 8, 10 lit. e y 39 de la LOPDP y su Reglamento General; adicionalmente, IA-01 tiene como base legal directa el derecho a explicación de decisiones automatizadas del Art. 20 LOPDP (RL-06).
*Artefacto: ERS, requisito RL-06; fichas de componentes de IA (campo "Datos de entrenamiento").*

## Métricas

**19. ¿Qué métrica salió peor y qué hicieron al respecto?**
*(Completar con la métrica, M1–M6, de menor cumplimiento y la acción de mejora aplicada, una vez cerrada la Tabla de auditoría — responsable: Fuertes.)*
*Artefacto: tabla de auditoría de calidad; comparación antes/después.*

**20. Enséñenme los conteos con los que calcularon la verificabilidad.**
*(Completar con los conteos base de M3 —requisitos con criterio BDD comprobable sobre requisitos totales— y la referencia exacta a la subsección del ERS — responsable: Fuertes.)*
*Artefacto: Tabla 3 (Conteos base del ERS); Anexo A (conteos auditables).*

**21. ¿Por qué el peso de M1 (completitud) es mayor que el de M5 (impacto de cambio)?**
Porque la completitud de atributos obligatorios es una condición de piso para que el resto de métricas sea calculable de forma confiable, mientras que el impacto de cambio se mide sobre una muestra y es más sensible a la elección de los cinco requisitos evaluados.
*Artefacto: instrumento de auditoría (pesos M1–M6).*

## Ética e integridad académica

**22. ¿Qué partes del informe fueron asistidas por IA y cómo las validaron?**
Cada sección declara la herramienta usada, el tipo de asistencia (redacción, revisión de estilo, generación de código) y el método de validación aplicado; las secciones evaluativas (análisis, conclusiones, justificaciones de decisiones de ingeniería) son producción propia verificada por el equipo.
*Artefacto: declaración de uso de inteligencia artificial por sección.*
