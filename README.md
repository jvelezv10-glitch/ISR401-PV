# ISR401-PV

Repositorio del Proyecto Fin de Curso (PFC) de Ingeniería de Requerimientos (ISR-401), paralelo B, SPA 2026–2027. Proyecto: **NEXORA**.

## Integrantes

| Integrante | Correo |
|---|---|
| Paca Pilataza Luis Alberto | lpacap@uteq.edu.ec |
| Vélez Vinces Jostin Gustavo | jvelezv10@uteq.edu.ec |

## Contenido

| Carpeta | Actividad | Archivo principal | PDF compilado |
|---|---|---|---|
| `PFC/E1/` | TA-PFC-E1: visión, alcance, partes interesadas, contexto y plan de elicitación | `main.tex` | `main.pdf` |
| `PFC/E1/instrumentos/` | Guion de entrevista y modelo de consentimiento informado | `guion-entrevista.tex`, `consentimiento/consentimiento-modelo.tex` | — |
| `PFC/E1/evidencias/` | Notas anonimizadas y `MANIFIESTO.md` de las evidencias privadas | — | — |
| `PFC/E1/modelos/` | Fuentes editables de los modelos | — | — |

## Cómo compilar `PFC/E1/main.tex`

| Elemento | Valor |
|---|---|
| Compilador | `pdflatex` + `bibtex` (TeX Live 2024 o posterior, o MiKTeX) |
| Archivo principal | `PFC/E1/main.tex` |
| Bibliografía | `PFC/E1/referencias.bib`, estilo `ieeetr` (IEEE) |
| Paquetes | `inputenc`, `fontenc`, `babel` (spanish), `mathptmx`, `geometry`, `array`, `tabularx`, `booktabs`, `xcolor`, `colortbl`, `enumitem`, `float`, `fancyhdr`, `caption`, `tikz`, `hyperref`; todos vienen en TeX Live completo y en Overleaf |

En una computadora, desde la carpeta del repositorio clonado:

```bash
cd PFC/E1
pdflatex main
bibtex main
pdflatex main
pdflatex main
```

En Overleaf: subir el contenido de `PFC/E1` (`main.tex` y `referencias.bib`), elegir *Compiler* = **pdfLaTeX** y *Main document* = **main.tex**, y pulsar **Recompilar** (Overleaf ejecuta BibTeX solo).

## Cómo compilar los instrumentos

Cada instrumento compila solo con **pdfLaTeX**, sin bibliografía:

```bash
cd PFC/E1/instrumentos
pdflatex guion-entrevista
cd consentimiento
pdflatex consentimiento-modelo
```

`consentimiento-modelo.tex` usa `consentimiento-preambulo.tex`, `consentimiento-cuerpo.tex` y `logo_uteq.png`, que están en la misma carpeta.
