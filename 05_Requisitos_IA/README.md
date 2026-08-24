# C3 - Requisitos de IA (Responsable: MENDOZA PARRAGA ANDY JOHEL)

Especificación de los 3 componentes de inteligencia artificial de MundiPets: IA-01 (compatibilidad de cruza), IA-02 (validación de imágenes de perfil), IA-03 (moderación de mensajes).

## Contenido

- **`fichas_componentes/`** — Ficha de 11 campos por componente (identificador, tarea, entradas/salidas, datos de entrenamiento, métricas de éxito, equidad, explicabilidad, riesgos/fallback, clasificación de riesgo, plan de monitoreo, trazas).
- **`requisitos_RF_RNF/`** — 27 requisitos (9 por componente: 3 RF + 3 RNF de rendimiento + 2 RNF de equidad + 1 RNF de explicabilidad), todos con umbral, unidad y método de comprobación.
- **`datos_entrenamiento/`** — Detalle ampliado de origen, volumen, etiquetado, sesgos conocidos y base legal de los datos de cada componente.
- **`etica_privacidad_riesgo/`** — Finalidad, minimización, consentimiento, seudonimización, supervisión humana y clasificación de riesgo conforme al Reglamento (UE) 2024/1689 y la LOPDP.
- **`plan_monitoreo/`** — Indicador, frecuencia, umbral de alerta por deriva y criterio de reentrenamiento/retirada por componente.

## Resultado

- 3 componentes justificados con evidencia documental propia (EV-XX del ERS).
- 27 requisitos, todos con umbral numérico verificable.
- Trazas entregadas a Morales Sánchez para la matriz de trazabilidad final (`04_Trazabilidad/`).
