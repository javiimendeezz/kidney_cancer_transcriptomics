# Análisis de Datos Transcriptómicos con R Markdown

Este proyecto realiza un **análisis avanzado de datos transcriptómicos** utilizando información del dataset **KIPAN**. Este conjunto de datos contiene información normalizada de expresión génica derivada de secuenciación RNA-Seq de alta calidad (Illumina HiSeq), específicamente los valores **RSEM** (RNA-Seq by Expectation Maximization). Estos datos son clave para investigaciones relacionadas con la biología del cáncer, al englobar información de múltiples tipos de cáncer de riñón (KIPAN: Kidney Pan-Cancer).

El proyecto incluye:
- **Validación cruzada (10-fold CV)** repetida para garantizar resultados robustos.
- Metodologías predictivas como redes neuronales y regresión penalizada para clasificar y analizar patrones moleculares.

## Objetivos del Proyecto

Este análisis está diseñado para:
- Identificar biomarcadores transcriptómicos relevantes en el cáncer de riñón.
- Evaluar el rendimiento de modelos predictivos en datos moleculares.

## Contenido del Proyecto

- **`kidney_cancer_transcriptomics.Rmd`**: Archivo principal en R Markdown que contiene el código y las instrucciones del análisis.
- **Dataset**: `KIPAN__illuminahiseq_rnaseqv2__Level_3__RSEM_genes_normalized.data.RData`, un conjunto de datos que proporciona perfiles transcriptómicos normalizados.
- **Repeticiones y validación**:
  - REP.INIT = 1: Primera repetición de validación cruzada.
  - REP.END = 3: Última repetición para robustez en resultados.

## Metodologías Empleadas

- **Redes neuronales**: Utilizadas para modelado predictivo y clasificación de perfiles transcriptómicos.
- **Regresión penalizada**: Aplicada para selección de características relevantes y reducción de sobreajuste.
- **Validación cruzada**: Implementación de 10-fold CV para evaluar de manera consistente los modelos generados.

## Requisitos

1. **R**: Versión 4.0 o superior.
2. **Paquetes de R**: Asegúrate de instalar los siguientes paquetes:

   ```R
   install.packages(c("pROC", "h2o", "uuid", "caret", "glmnet"))
   ```

   Nota: La instalación de `h2o` puede requerir un tiempo adicional debido a su tamaño.

3. **RStudio**: Opcional, para facilitar la edición y ejecución del archivo.

## Instrucciones de Uso

1. **Abrir el archivo**:
   - Carga `tarea1.Rmd` en RStudio.

2. **Ejecutar el archivo**:
   - Haz clic en el botón "Knit" para generar la salida HTML.

3. **Revisar los resultados**:
   - El archivo HTML generado contendrá los gráficos, tablas y resultados del análisis.

## Notas

- Durante la instalación de paquetes, puede ser necesario aumentar el tiempo de espera predeterminado en R para la descarga de paquetes grandes como `h2o`. Usa el siguiente comando si es necesario:

  ```R
  options(timeout = 120)
  ```

## Impacto Biológico

Este análisis permite explorar profundamente la expresión génica en diferentes tipos de cáncer de riñón. Los resultados pueden ayudar a identificar biomarcadores clave para diagnóstico, pronóstico y posibles dianas terapéuticas.


