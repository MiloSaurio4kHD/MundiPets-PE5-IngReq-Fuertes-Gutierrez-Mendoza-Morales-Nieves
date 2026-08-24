# MundiPets — PE5, Unidad 5: Integración, Métricas y Defensa del Proyecto Integrador

**Sistema del PFC:** MundiPets — plataforma de adopción y cruza responsable de mascotas
**Asignatura:** Ingeniería de Requisitos (ISR-401) — UTEQ — 2026-2027 PPA
**Entrega:** PE5 / Unidad 5
**Repositorio de esta entrega:** https://github.com/MiloSaurio4kHD/MundiPets-PE5-IngReq-Fuertes-Gutierrez-Mendoza-Morales-Nieves
**Repositorio del PFC base (ERS, UML, PE1–PE4):** https://github.com/andymendozap03/MundiPets-PFC-IngReq

## Integrantes

| Integrante | Rol | Criterio principal |
|---|---|---|
| FUERTES ARRAES, Edson Daniel | Analista líder | C1 — Auditoría de calidad del ERS con métricas |
| MORALES SÁNCHEZ, Gary Alejandro | Documentador | C2 — Trazabilidad end-to-end y matriz final |
| MENDOZA PÁRRAGA, Andy Johel | Modelador | C3 — Especificación de requisitos de IA |
| GUTIÉRREZ ORTEGA, Génesis Adriana | Verificador | C4 — ERS/SRS final integrado; C7 — Referencias |
| NIEVES SÁNCHEZ, Jimmy Samuel | Verificador | C5 — Coordinación de la defensa; gestión del repositorio |

## Cómo regenerar el PDF (criterio de piso G2)

### Dependencias

- TeX Live 2023 o superior (o MiKTeX 23+)
- Motor: **pdflatex**
- Bibliografía: **biber** + **biblatex** (estilo IEEE, `backend=biber`)
- Paquetes: IEEEtran, babel (spanish), csquotes, hyphenat, booktabs, tabularx, array, multirow, longtable, graphicx, float, pdflscape, xcolor, mdframed, geometry, fancyhdr, parskip, enumitem, amsmath, amssymb, titlesec, caption, hyperref, url

### Archivo principal

`01_Informe_Final/PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex`

Requiere `referencias.bib` en la misma carpeta.

> **Nota de verificación:** al momento de redactar este README, `referencias.bib` no aparecía en `01_Informe_Final/` en la copia local verificada. Confirmar que el archivo esté presente en el repositorio remoto antes de dar por cerrado el piso G2 — sin él, `biber` no resuelve las citas y estas aparecen como `[?]`.

### Orden exacto de comandos

```bash
git clone https://github.com/MiloSaurio4kHD/MundiPets-PE5-IngReq-Fuertes-Gutierrez-Mendoza-Morales-Nieves.git
cd MundiPets-PE5-IngReq-Fuertes-Gutierrez-Mendoza-Morales-Nieves/01_Informe_Final

pdflatex PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex
biber    PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves
pdflatex PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex
pdflatex PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex
```

Sin el paso de `biber`, las citas aparecen como `[?]` y la bibliografía no se genera.

Alternativa en un solo paso: `latexmk -pdf PE5_U5_PFC_Final_Fuertes_Gutierrez_Mendoza_Morales_Nieves.tex` (requiere configurar `%.pdf: %.tex` con biber en `latexmkrc`).

## Estructura del repositorio

```
00_Gestion/           Plan de trabajo, actas, retrospectiva, aporte individual
01_Informe_Final/     .tex + .pdf del informe PE5 (archivo principal)
02_ERS_Final/         Versión final consolidada del ERS/SRS (Responsable: Gutiérrez)
03_Metricas/          Instrumento de auditoría, conteos base, cálculos M1–M6 (Fuertes)
04_Trazabilidad/      Matriz final, huérfanos, sincronización con el backlog (Morales)
05_Requisitos_IA/     Fichas de componentes de IA, RF/RNF, ética y monitoreo (Mendoza)
06_Defensa/           Presentación, banco de preguntas, guion y tiempos (Todos)
07_Modelos_UML/       Modelos UML vigentes, PNG/SVG + fuentes editables (Morales)
08_Evidencias/        Capturas del tablero, historial de commits, PE4
scripts/              Utilidades (conteos, validaciones, compilación)
```

> **Nota de verificación:** la carpeta `09_Entregable_SGA/` mencionada en versiones previas de este README no existe todavía en el repositorio verificado. Si la guía exige un PDF final con nombre específico para el SGA, crearla antes de la entrega.

## Línea base

La línea base final se etiqueta en Git como `v5.0-PE5-baseline`, anclada al commit `e0d0545` (versión 4.0 del ERS, congelada el 30/08/2026). Ver Sección 6.1 del informe para el detalle completo y el comando de verificación.

## Reglas de trabajo en Git

- Cada integrante hace commit con su propia cuenta.
- Mínimo dos commits por semana por persona.
- Mensajes descriptivos tipo `feat(ámbito): descripción breve` (ejemplo: `feat(metricas): calculo de M3 con conteos base`).
- Una rama por criterio de la rúbrica: `c1-metricas`, `c2-trazabilidad`, `c3-ia`, `c4-ers`, `c6-informe`.
- Integración a `main` únicamente por Pull Request; nunca un commit único de carga masiva al final.

## Declaración de uso de IA

Ver Anexo E del informe (`01_Informe_Final/...tex`), sección "Referencias y Declaración de Uso de Inteligencia Artificial".

## Licencia y citación

Ver `CITATION.cff` para el formato de cita del trabajo.
