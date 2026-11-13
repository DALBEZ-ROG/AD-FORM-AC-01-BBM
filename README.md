# FORM-AC-01: Análisis de caso de un fallo real en un sistema distribuido

Universidad Técnica Estatal de Quevedo, Carrera de Software.
Aplicaciones Distribuidas (ISR-701), séptimo nivel, paralelo B.
Docente: Gleiston Guerrero Ulloa, PhD.

## Integrantes

- Benites Pérez Dariem Alberto (DALBEZ-ROG)
- Bueno Troya Erwin Daniel (Troyano2004)
- Mendoza Villarroel Elian Jossue (Elianmen123)

## Caso analizado

La caída de Facebook, Instagram y WhatsApp del 4 de octubre de 2021. La fuente principal es el informe oficial de Meta, *More details about the October 4 outage*:
https://engineering.fb.com/2021/10/05/networking-traffic/outage-details/

## Contenido del repositorio

| Carpeta | Archivos |
|---|---|
| `caratula/` | `caratula.tex` y `caratula.pdf` |
| `documento/` | `main.tex`, `referencias.bib`, `main.bbl` y `main.pdf` |
| `documento/secciones/` | Un archivo `.tex` por apartado del análisis |
| `diagrama/` | `ishikawa.drawio` (editable en draw.io o app.diagrams.net) y `ishikawa.pdf` |

## Cómo compilar

Se necesita MiKTeX o TeX Live con `pdflatex`, `biber` y los paquetes `biblatex` y `biblatex-ieee`. Las referencias están en formato IEEE.

**Documento**

`main.tex` incluye las secciones de `documento/secciones/` y el PDF del diagrama, así que se compila con el repositorio completo y desde la carpeta `documento`:

```
cd documento
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Si no hay `biber`, el repositorio incluye `main.bbl`, y con dos pasadas de `pdflatex` las referencias salen igual.

**Carátula**

```
cd caratula
pdflatex caratula.tex
```

## Uso de IA

Lo que se hizo con IA está declarado al final de `documento/main.pdf`.
