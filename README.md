# TFM: Comparación entre modelos físicos y modelos de aprendizaje automático para la estimación de la irradiancia solar

## Descripción

Trabajo Fin de Máster del **Máster Universitario en Big Data y Ciencia de Datos** de la Universidad Internacional de Valencia (VIU).

Este proyecto compara modelos paramétricos tradicionales (Erbs, Kasten, Maxwell, Perez) con algoritmos de aprendizaje automático (Ridge, Random Forest, Gradient Boosting, SVR, MLP, kNN) y una arquitectura híbrida de dos etapas para la estimación de la irradiancia directa normal (DNI) a partir de la irradiancia global horizontal (GHI).

## Estructura del repositorio

*   `Modelos_de_predicción.ipynb` — Notebook con el flujo experimental completo.
*   `declaraciones_ia/` — Documentos formales sobre el uso de herramientas de IA generativa.
*   `data/` — Datos del NSRDB (o instrucciones de descarga).
*   `README.md` — Este archivo.

## Datos

Los datos proceden del National Solar Radiation Database (NSRDB) del NREL, correspondientes al año 2019 para seis ciudades europeas:

| Ciudad | Clima | Rol |
| :--- | :--- | :--- |
| Almería | Semiárido | Entrenamiento |
| Santa Cruz de Tenerife | Subtropical | Entrenamiento |
| Galway | Oceánico | Test |
| Grenoble | Alpino | Test |
| Milán | Continental urbano | Test |
| Viena | Continental templado | Test |

Los datos pueden descargarse directamente desde el portal oficial: https://nsrdb.nrel.gov

## Requisitos

*   Python 3.x
*   pandas
*   numpy
*   scikit-learn
*   matplotlib
*   seaborn

## Ejecución

1. Abrir `Modelos_de_predicción.ipynb` en Google Colab o Jupyter Notebook.
2. Subir los 6 archivos CSV cuando el entorno lo solicite.
3. Ejecutar todas las celdas en orden secuencial.

## Autora

**Sabrina Khan Navarro**

## Declaración de uso de IA

En la elaboración de este proyecto se han empleado herramientas de inteligencia artificial generativa (Claude, Gemini, Consensus) estrictamente como apoyo técnico y metodológico. El detalle formal de este soporte se encuentra documentado en la carpeta `declaraciones_ia/` de este repositorio y en el Anexo A de la memoria. El diseño de la investigación, el análisis crítico de los datos y la interpretación de los resultados son de elaboración exclusiva de la autora.

## Licencia

MIT License
