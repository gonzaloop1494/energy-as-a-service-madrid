# Energy-as-a-Service para viviendas en Madrid

Repositorio del trabajo **Energy-as-a-Service para viviendas en Madrid: arquitectura IoT hibrida edge + cloud para ahorro energetico en climatizacion**.

El proyecto propone una solucion domotica para una vivienda tipo en Madrid basada en sensores, hub local, control HVAC y servicios cloud. El objetivo es reducir el consumo de climatizacion sin perder confort, manteniendo privacidad, resiliencia local y viabilidad como servicio por suscripcion.

## Contenido

- [`poster/poster.pdf`](poster/poster.pdf): poster final.
- [`poster/poster.tex`](poster/poster.tex): fuente LaTeX que inserta el poster final en PDF.
- [`poster/poster_source.pdf`](poster/poster_source.pdf): PDF fuente insertado por LaTeX.
- [`poster/figures/`](poster/figures): figuras principales del poster.
- [`docs/guion_exposicion.md`](docs/guion_exposicion.md): guion de exposicion en Markdown.
- [`docs/guion_exposicion_desarrollado.pdf`](docs/guion_exposicion_desarrollado.pdf): guion desarrollado.
- [`docs/guion_exposicion_gonzalo_pacheco.pdf`](docs/guion_exposicion_gonzalo_pacheco.pdf): version PDF del guion.
- [`docs/notas_metodologia.md`](docs/notas_metodologia.md): notas sobre alcance, supuestos y criterios tecnicos.
- [`docs/bibliografia.pdf`](docs/bibliografia.pdf): bibliografia.
- [`assets/`](assets): logo URJC y QR de bibliografia.

## Estructura

```text
.
├── README.md
├── poster/
│   ├── poster.tex
│   ├── poster.pdf
│   ├── poster_source.pdf
│   └── figures/
├── docs/
│   ├── README.md
│   ├── guion_exposicion.md
│   ├── guion_exposicion_desarrollado.pdf
│   ├── guion_exposicion_gonzalo_pacheco.pdf
│   ├── notas_metodologia.md
│   └── bibliografia.pdf
└── assets/
    ├── logo_urjc.png
    ├── qr_bibliografia.png
    └── qr_repo.png
```

## Compilacion del poster

Desde la carpeta `poster/`:

```bash
pdflatex poster.tex
```

El archivo `poster.tex` utiliza `pdfpages` para preservar exactamente el aspecto del poster final en PDF.

## Autor

Gonzalo Pacheco Agredano  
Universidad Rey Juan Carlos, Escuela de Ingenieria de Fuenlabrada  
Asignatura: Comunicaciones Sectoriales
