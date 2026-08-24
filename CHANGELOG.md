# Changelog — PE5 MundiPets

Formato: [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/). Versionado del ERS y del informe de la PE5.

## [v5.0-PE5-baseline] — 2026-08-30

Línea base final de la entrega, anclada al commit `e0d0545`.

### Added
- Informe final PE5 completo (Secciones 1–11, Fundamento Teórico, Anexos A–F), archivo `01_Informe_Final/PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex`.
- ERS versión 4.0 consolidado en `02_ERS_Final/`, con revisión de calidad de RF-02, RF-05, RF-12, RF-17, RF-18 y RF-23, e incorporación de RF-26 y RF-27 (evidencia EV-23, EV-24).
- Sección 7 completa: identificación y justificación de 3 componentes de IA (IA-01 compatibilidad de cruza, IA-02 validación de imágenes, IA-03 moderación de mensajes), fichas de 11 campos, 27 requisitos RF-IA/RNF-IA con umbral y método de comprobación, ética/privacidad/riesgo, plan de monitoreo.
- Matriz de trazabilidad final con 43 elementos vigentes (27 RF, 16 RNF), 0 requisitos huérfanos.
- Auditoría de calidad con seis métricas (M1–M6) y aritmética visible; M6 = 0,00 (óptimo), M1a = 44,26 % (por debajo de referencia).
- Banco completo de 22 preguntas del tribunal con respuesta preparada y artefacto de respaldo (Anexo B).
- Resumen bilingüe (español/inglés), 200 palabras cada uno, con formato IEEE manual unificado.
- Sección 11.2 "Reglas de la defensa" con la verificación previa obligatoria de 4 preguntas por integrante.

### Fixed
- Corrección de la técnica de elicitación declarada: entrevista semiestructurada (no estructurada), y actualización del cuestionario a 61 respuestas válidas.
- Corrección de tablas de la Sección 6 (matriz de trazabilidad, diagnóstico de huérfanos, registro de RFC) de `table[H]` a `longtable`, para respetar los márgenes de página y permitir salto entre páginas.
- Corrección de columnas `X` inválidas dentro de `longtable` (solo válidas en `tabularx`), causante del error "Extra alignment tab has been changed to \\cr".
- Corrección de `\setlength{\jot}{8pt}` agrupado alrededor de entornos `align*` en la Sección 8.2, causante del error "Incompatible glue units".
- Adición de `\spanishplainpercent` tras cargar `babel[spanish]`, para evitar el conflicto entre la macro `\es@sppercent` y los entornos `align*` de `amsmath`.
- Corrección de `\appendix` a `\appendices` (comando nativo de IEEEtran), para que los anexos se numeren con letras (A, B, C…) en vez de mostrar un heading genérico sin numerar.
- Eliminación de un `\begin{table}[H]` anidado inválidamente alrededor de un `\begin{longtable}` en el Anexo E, causante de desborde de márgenes y de un `\caption` duplicado.
- Corrección de referencias cruzadas rotas: `\ref{sec:req_ia}` → `\ref{sec:requisitos_ia}`; adición del `\label{sec:metricas}` faltante en la Sección 8.
- Restauración del bloque de portada con el repositorio del PFC base, perdido en una fusión de ramas.
- Actualización del hash de commit declarado en la Tabla 3.3 y la Sección 6.1, de `8b1970d` (provisional) a `55f11d9` (real).

### Changed
- Uniformado el sujeto de los 27 requisitos RF-IA/RNF-IA a "El sistema deberá…".
- Reescrito el bloque de resumen/abstract con formato manual IEEE (`\textbf{Resumen---}` / `\textbf{Abstract---}`) en vez del entorno automático `\begin{abstract}`, que no reconocía el idioma español.

## [No publicado]

### Added
- Estructura inicial del repositorio de la PE5.
- Preámbulo LaTeX base y `referencias.bib`.
