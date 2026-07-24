# TFM: Comparación entre modelos físicos y modelos de aprendizaje automático para la estimación de la irradiancia solar

## Descripción

Trabajo Fin de Máster del Máster Universitario en Big Data y Ciencia de Datos
de la Universidad Internacional de Valencia (VIU).

Este proyecto compara modelos paramétricos tradicionales (Erbs, Kasten, Maxwell,
Perez) con algoritmos de aprendizaje automático (Ridge, Random Forest, Gradient
Boosting, SVR, MLP, kNN) y una arquitectura híbrida de dos etapas para la
estimación de la irradiancia directa normal (DNI) a partir de la irradiancia
global horizontal (GHI).

## Estructura del repositorio

- `Modelos_de_predicción.ipynb` — Notebook con el flujo experimental completo
- `prompts/` — Registro de interacciones con herramientas de IA generativa
- `data/` — Datos del NSRDB (o instrucciones de descarga)
- `README.md` — Este archivo

## Datos

Los datos proceden del National Solar Radiation Database (NSRDB) del NREL,
correspondientes al año 2019 para seis ciudades europeas:

| Ciudad | Clima | Rol |
|--------|-------|-----|
| Almería | Semiárido | Entrenamiento |
| Santa Cruz de Tenerife | Subtropical | Entrenamiento |
| Galway | Oceánico | Test |
| Grenoble | Alpino | Test |
| Milán | Continental urbano | Test |
| Viena | Continental templado | Test |

Los datos pueden descargarse desde https://nsrdb.nrel.gov

## Requisitos

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Ejecución

1. Abrir `Modelos_de_predicción.ipynb` en Google Colab o Jupyter Notebook
2. Subir los 6 archivos CSV cuando se solicite
3. Ejecutar todas las celdas en orden

## Autora

Sabrina Khan Navarro

## Declaración de uso de IA

En la elaboración de este proyecto se han empleado herramientas de IA generativa
(Claude, Gemini, Consensus) como apoyo. El detalle se encuentra en la carpeta
`prompts/` y en el Anexo A de la memoria. El diseño, análisis e interpretación
son de elaboración propia.

## Licencia

MIT License
