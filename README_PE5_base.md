# PE5 - Integracion, Metricas y Defensa del Proyecto Integrador

**Sistema del PFC:** MundiPets - plataforma de adopcion y cruza responsable de mascotas
**Asignatura:** Ingenieria de Requisitos (ISR-401) - UTEQ - 2026-2027 PPA
**Entrega:** PE5 / Unidad 5
**Repositorio de esta entrega:** https://github.com/USUARIO/MundiPets-PE5-IngReq-UTEQ
**Repositorio del PFC base (ERS, UML, PE1-PE4):** https://github.com/andymendozap03/MundiPets-PFC-IngReq

## Integrantes

- FUERTES ARRAES EDSON DANIEL
- GUTIERREZ ORTEGA GENESIS ADRIANA
- MENDOZA PARRAGA ANDY JOHEL
- MORALES SANCHEZ GARY ALEJANDRO
- NIEVES SANCHEZ JIMMY SAMUEL

## Como regenerar el PDF (criterio de piso G2)

### Dependencias

- TeX Live 2023 o superior (o MiKTeX 23+)
- Motor: **pdflatex**
- Bibliografia: **biber** + **biblatex** (estilo IEEE, backend=biber)
- Paquetes: IEEEtran, babel (spanish), csquotes, hyphenat, booktabs,
  tabularx, array, multirow, longtable, graphicx, float, pdflscape,
  xcolor, mdframed, geometry, fancyhdr, parskip, enumitem, amsmath,
  amssymb, titlesec, caption, hyperref, url

### Archivo principal

`01_Informe_Final/PE5_U5_Trabajo_Dividido.tex`

Requiere `referencias.bib` en la misma carpeta (ya incluido en
`01_Informe_Final/`).

### Orden exacto de comandos

```bash
git clone https://github.com/USUARIO/MundiPets-PE5-IngReq-UTEQ.git
cd MundiPets-PE5-IngReq-UTEQ/01_Informe_Final
pdflatex PE5_U5_Trabajo_Dividido.tex
biber    PE5_U5_Trabajo_Dividido
pdflatex PE5_U5_Trabajo_Dividido.tex
pdflatex PE5_U5_Trabajo_Dividido.tex
```

Sin el paso de `biber`, las citas aparecen como `[?]` y la
bibliografia no se genera.

Alternativa en un solo paso: `latexmk -pdf PE5_U5_Trabajo_Dividido.tex`
(requiere configurar `%.pdf: %.tex` con biber en `latexmkrc`).

## Estructura del repositorio

```
00_Gestion/           Plan de trabajo, actas, retrospectiva, aporte individual
01_Informe_Final/     PE5_U5_Trabajo_Dividido.tex + referencias.bib (archivo principal)
02_ERS_Final/         Version final consolidada del ERS/SRS (Responsable: Gutierrez)
03_Metricas/          Instrumento de auditoria, conteos base, calculos M1-M6 (Fuertes)
04_Trazabilidad/      Matriz final, huerfanos, sincronizacion con el backlog (Morales)
05_Requisitos_IA/     Fichas de componentes de IA, RF/RNF, etica y monitoreo (Mendoza)
06_Defensa/           Presentacion, banco de preguntas, guion y tiempos (Todos)
07_Modelos_UML/       Modelos UML vigentes, PNG/SVG + fuentes editables (Morales)
08_Evidencias/        Capturas del tablero, historial de commits, PE4
09_Entregable_SGA/    PDF final con el nombre exigido por la guia
scripts/              Utilidades (conteos, validaciones, compilacion)
```

## Linea base

La linea base final se etiqueta en Git como `v5.0-PE5-baseline`.

## Declaracion de uso de IA

Ver `01_Informe_Final/anexos/anexo_E_referencias_declaracion_IA.tex`
(dentro del .tex principal, Anexo E).
