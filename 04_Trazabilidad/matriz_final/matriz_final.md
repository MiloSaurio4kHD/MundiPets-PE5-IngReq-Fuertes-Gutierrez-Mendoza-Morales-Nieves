# Matriz de trazabilidad final del ERS de MundiPets

Consolida la trazabilidad end-to-end de los 43 elementos vigentes del ERS (27 RF y 16 RNF), siguiendo la cadena mínima exigida para el PFC: Fuente/Stakeholder, RF/RNF, CU, Clase UML, Proceso DFD, Estado, Criterio BDD, Caso de Prueba conceptual e Historia del backlog, más una columna de trazabilidad horizontal (relación entre requisitos del mismo nivel) solicitada adicionalmente por el docente.

El Proceso DFD corresponde a los seis procesos del Diagrama de Flujo de Datos Nivel 1 (P1 a P6), que descompone el proceso único "0. MundiPets" del Diagrama de Contexto. La columna Fuente identifica al participante de origen mediante su código de evidencia (PROP-XX para propietarios, VET-XX para veterinarias, OBS-01 para la observación de campo y Encuesta para el cuestionario digital agregado), conforme lo solicitó el docente en lugar del identificador EV-XX. Un enlace se marca únicamente cuando existe evidencia textual verificable en el ERS o en los modelos del sistema; los eslabones sin relación real se marcan con "—".

| RF/RNF | Fuente | Horizontal | CU | Clase UML | DFD | Estado | BDD | CP | Hist. | Estado de la traza |
|---|---|---|---|---|---|---|---|---|---|---|
| RF-01 | PROP-02, VET-01, VET-03, OBS-01 | RF-12 | CU-01 | Pet | P1 | Perfil Mascota | CA-01 | CP-01 | HU-01 | Completa |
| RF-02 | PROP-01, VET-02 | RF-14 | CU-02 | MedicalHistory, Pet | P2 | — | CA-02 | CP-02 | HU-02 | Completa |
| RF-03 | VET-02, PROP-03, OBS-01 | RF-11 | CU-10 | Pet, MedicalHistory | P2 | — | CA-03 | CP-03 | HU-03 | Completa |
| RF-04 | Encuesta, OBS-01 | — | CU-11 | Post, Pet | P3 | — | — | CP-04 | — | Completa (Should) |
| RF-05 | PROP-01, PROP-02, VET-01, OBS-01 | RF-13 | CU-04 | Post | P3 | Perfil Mascota | CA-04 | CP-05 | HU-04 | Completa |
| RF-06 | VET-02, VET-03, PROP-03, OBS-01 | RNF-13, RF-02, RF-16 | CU-13 | CompatibilityEvaluation, Pet | P4 | — | CA-05 | CP-06 | HU-05 | Completa |
| RF-07 | PROP-02, Encuesta, OBS-01 | RNF-15 | CU-08 | Message | P5 | — | — | CP-07 | — | Completa (Could) |
| RF-08 | PROP-01, VET-01, VET-03 | RF-27 | CU-05 | BreedingRequest | P3 | Solicitudes | CA-06 | CP-08 | HU-06 | Completa |
| RF-09 | VET-01, VET-03, Encuesta | RF-26, RF-19 | CU-09 | VeterinaryEvaluation, MedicalHistory | P2 | Verif. Documentos | CA-07 | CP-09 | HU-07 | Completa |
| RF-10 | PROP-02, VET-02, PROP-03 | RD-08 | CU-12 | Pet, PetVaccine | P5 | — | — | CP-10 | — | Completa (Should) |
| RF-11 | PROP-02, VET-03, PROP-03, Encuesta, OBS-01 | RF-03, RNF-01, RNF-16 | CU-06 | PrivacySettings | P1 | — | CA-08 | CP-11 | HU-08 | Completa |
| RF-12 | PROP-01, VET-01, Encuesta, OBS-01 | RF-01 | (Onboarding) | User | P1 | — | CA-09 | CP-12 | HU-09 | Completa |
| RF-13 | PROP-01, PROP-02, Encuesta, OBS-01 | RF-05 | CU-04 | Post | P3 | — | CA-10 | CP-13 | HU-10 | Completa |
| RF-14 | VET-01, VET-03, Encuesta | RF-02, RF-24 | CU-03 | PetVaccine, VetDocument | P2 | Verif. Documentos | CA-11 | CP-14 | HU-11 | Completa |
| RF-15 | PROP-01, PROP-02, VET-02, PROP-03 | RF-27 | CU-07 | AdoptionRequest, BreedingRequest | P3 | Solicitudes | — | CP-15 | — | Completa (Should) |
| RF-16 | PROP-01, VET-01, VET-03, Encuesta | RF-06 | CU-02 | Pet | P2 | — | CA-12 | CP-16 | HU-12 | Completa |
| RF-17 | PROP-01, VET-01, Encuesta, OBS-01 | RNF-06, RNF-07 | (Publicaciones) | Post | P6 | — | — | CP-17 | — | Completa (Should) |
| RF-18 | PROP-06, VET-05 | RF-05 | CU-04 | Post | P3 | Perfil Mascota | CA-13 | CP-18 | HU-13 | Completa |
| RF-19 | PROP-06 | RF-09 | CU-09 | VetDocument, VeterinaryEvaluation | P2 | Verif. Documentos | — | CP-19 | — | Completa (Should) |
| RF-20 | PROP-08 | — | CU-08 | Message, Interaction | P5 | — | — | CP-20 | — | Completa (Could) |
| RF-21 | VET-05 | — | CU-01 | Pet | P1 | — | — | CP-21 | — | Completa (Should) |
| RF-22 | PROP-05, VET-05 | — | CU-07 | AdoptionRequest | P3 | Solicitudes | CA-14 | CP-22 | HU-14 | Completa |
| RF-23 | PROP-04, PROP-07, VET-04, PROP-11 | — | CU-06 | Interaction, BreedingRequest | P4 | — | CA-15 | CP-23 | HU-15 | Completa |
| RF-24 | VET-04, VET-05 | RF-14 | CU-03 | PetVaccine | P2 | — | — | CP-24 | — | Completa (Should) |
| RF-25 | PROP-07, VET-05 | RNF-16 | CU-04 | Post | P3 | Perfil Mascota | — | CP-25 | — | Completa (Could) |
| RF-26 | VET-07 | RF-09 | CU-09 | VeterinaryEvaluation | P2 | Verif. Documentos | — | CP-26 | — | Completa (Should) |
| RF-27 | PROP-12 | RF-08, RF-15 | CU-05 | BreedingRequest | P3 | Solicitudes | — | CP-27 | — | Completa (Should) |
| RNF-01 | VET-03, PROP-03, Encuesta, OBS-01 | RF-11, RNF-16, RD-04, RNF-05 | CU-06 | — | P1 | — | — | CP-28 | — | Completa (transversal) |
| RNF-02 | PROP-01, PROP-02, VET-01, VET-02, VET-03, PROP-03, Encuesta | RNF-03 | (Transversal) | — | Transversal | — | — | CP-29 | — | Completa (transversal) |
| RNF-03 | PROP-01, PROP-02, VET-01, VET-02, VET-03, PROP-03, Encuesta | RNF-02 | CU-11 | — | Transversal | — | — | CP-30 | — | Completa (transversal) |
| RNF-04 | PROP-01, PROP-02, VET-01, VET-02, VET-03, PROP-03, Encuesta, OBS-01 | — | (UI) | — | Transversal | — | — | CP-31 | — | Completa (transversal) |
| RNF-05 | VET-01, VET-03, Encuesta | RD-04, RNF-01 | CU-02 | — | P2 | — | — | CP-32 | — | Completa (transversal) |
| RNF-06 | PROP-01, VET-01, VET-03, Encuesta | RF-06, RNF-13 | CU-13 | — | P4 | — | — | CP-33 | — | Completa (transversal) |
| RNF-07 | PROP-01, VET-01, VET-03, Encuesta | RNF-06 | (Media) | — | P6 | — | — | CP-34 | — | Completa (transversal) |
| RNF-08 | PROP-01, PROP-02, VET-01, VET-02, VET-03, PROP-03, Encuesta | — | CU-01 | — | P1 | — | — | CP-35 | — | Completa (transversal) |
| RNF-09 | PROP-04, PROP-11 | RD-08, RF-10 | CU-12 | — | P5 | — | — | CP-36 | — | Completa (transversal) |
| RNF-10 | Derivado del equipo | — | (Diseño) | — | Transversal | — | — | CP-37 | — | Completa (transversal) |
| RNF-11 | Encuesta, OBS-01 | — | (UI) | — | Transversal | — | — | CP-38 | — | Completa (transversal) |
| RNF-12 | Encuesta, OBS-01 | RNF-03 | (Transversal) | — | Transversal | — | — | CP-39 | — | Completa (transversal) |
| RNF-13 | PROP-06, PROP-08, VET-04, VET-05 | RF-06, RNF-06, RNF-14 | CU-13 | — | P4 | — | — | CP-40 | — | Completa (transversal) |
| RNF-14 | PROP-06, PROP-08 | RF-06, RNF-13 | (Media) | — | P6 | — | — | CP-41 | — | Completa (transversal) |
| RNF-15 | PROP-08, PROP-11 | RF-06, RNF-13, RF-07 | CU-08 | — | P5 | — | — | CP-42 | — | Completa (transversal) |
| RNF-16 | PROP-07, VET-05 | RF-11, RNF-01, RD-02, RF-25 | CU-06 | — | P1 | — | — | CP-43 | — | Completa (transversal) |

## Resumen

De los 43 elementos evaluados, el 100 % cuenta con fuente identificada y al menos un CU o designación transversal. Cero requisitos huérfanos detectados.
