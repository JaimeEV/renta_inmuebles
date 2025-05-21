# 📊 Análisis de Rentas Residenciales en la Ciudad de México

## 🏙️ Introducción

Encontrar un departamento en la Ciudad de México (CDMX) es a menudo una tarea desafiante. Uno de los mayores retos es determinar si el precio de una renta es justo, o si estamos pagando de más o de menos en comparación con el promedio de la zona. Frecuentemente, esta valoración se basa en la intuición o en consejos de conocidos, lo que se conoce como "a ojo de buen cubero".

Este proyecto busca abordar esta problemática mediante un análisis de datos de departamentos en renta extraídos de diversas fuentes de internet. El objetivo principal es identificar y visualizar los rangos de precios predominantes en distintas alcaldías de la CDMX, proporcionando una perspectiva más informada sobre el mercado de alquileres.

Es importante destacar que los datos utilizados en este análisis son **ficticios** (*dummy data*), creados con fines educativos y para demostrar el proceso analítico.

**[➡️ Ver el Notebook renderizado en nbviewer](https://nbviewer.org/github/JaimeEV/renta_inmuebles/blob/main/Analisis_inmuebles.ipynb)**
*(Recomendado para una lectura más amigable, especialmente si no estás familiarizado con los archivos .ipynb)*

**[📂 Ver el código fuente en GitHub](https://github.com/JaimeEV/renta_inmuebles/blob/main/Analisis_inmuebles.ipynb)**
*(Para revisar el código Python y la estructura del notebook)*

---

## 🎯 Objetivos del Análisis

* Limpiar y preparar un conjunto de datos de rentas de inmuebles para el análisis.
* Explorar la distribución general de los precios de renta de departamentos en la CDMX.
* Identificar y analizar valores atípicos en los precios.
* Determinar un rango de precios donde se concentra la mayoría de las rentas.
* Analizar y comparar los precios y tamaños promedio de los departamentos en las principales alcaldías por volumen de oferta.
* Investigar la correlación entre el precio de renta y los metros cuadrados de construcción.

---

## 🛠️ Herramientas Utilizadas

* **Lenguaje de Programación:** Python
* **Librerías de Análisis y Manipulación de Datos:**
    * Pandas
* **Librerías de Visualización de Datos:**
    * Matplotlib
    * Seaborn

---

## 📈 Hallazgos Clave del Notebook

El análisis de los datos (ficticios) arrojó varios insights sobre el mercado de rentas de departamentos en la CDMX:

1.  **Distribución de Precios:** La distribución de los precios de renta presenta un **sesgo hacia la derecha**, lo que sugiere que, aunque la mayoría de los departamentos se concentran en rangos de precios más bajos, existen propiedades con rentas considerablemente más altas que influyen en el promedio.
2.  **Valores Atípicos y Rango Típico:**
    * La mediana de los precios de renta fue de **\$13,750.00**, mientras que el promedio se situó en **\$14,913.15**, confirmando la influencia de los valores atípicos.
    * Se estimó que el 95% de las rentas se encuentran aproximadamente entre **\$1,098 y \$28,598**. Se observó que el límite inferior podría incluir ofertas de habitaciones, lo que requeriría una segmentación más fina en un análisis con datos reales.
3.  **Análisis por Alcaldía:**
    * Se identificaron las 5 alcaldías con mayor número de departamentos registrados (en el dataset sin atípicos de precio) para un análisis más detallado, siendo estas (ejemplos basados en el análisis): Benito Juárez, Cuauhtémoc, Álvaro Obregón, Coyoacán y Tlalpan. *(Nota: El notebook identifica las top 5 basadas en el conteo del dataset filtrado).*
    * Existen variaciones notables en los rangos de precios y la presencia de valores atípicos incluso a nivel de alcaldía, lo que indica una heterogeneidad en el mercado dentro de las mismas demarcaciones.
4.  **Correlación Precio vs. Superficie:**
    * Se observó una **clara relación positiva** entre el precio de renta y los metros cuadrados de construcción: a mayor superficie, mayor tiende a ser el precio.
    * La gráfica de dispersión también mostró valores atípicos, sugiriendo posibles "buenas oportunidades" (mayor superficie a menor precio relativo) o propiedades sobrevaloradas.
5.  **Tamaño Promedio por Alcaldía:**
    * Se encontraron diferencias en el tamaño promedio (m² de construcción) de los departamentos entre las principales alcaldías. Por ejemplo, en el análisis, Benito Juárez tendía a tener departamentos más grandes en promedio en comparación con otras como Cuauhtémoc o Iztacalco.

---

## 💡 Consideraciones y Posibles Próximos Pasos

* La presencia de valores atípicos en precios y la posible inclusión de rentas de habitaciones en el rango inferior de precios destacan la importancia de una cuidadosa segmentación y limpieza de datos en análisis reales.
* La heterogeneidad de precios dentro de las mismas alcaldías sugiere que análisis más granulares (a nivel de colonia) serían valiosos.
* **Próximos Pasos (con datos reales):**
    * Incorporar más variables como antigüedad del inmueble, número de recámaras/baños, amenidades, etc.
    * Realizar un análisis de series temporales si se dispone de fechas de publicación.
    * Desarrollar un modelo predictivo de precios de renta.

---
## 🚀 Cómo Visualizar y Ejecutar el Notebook

1.  **Opción Recomendada (Visualización Rápida):**
    * Haz clic en el enlace de **nbviewer** proporcionado al inicio de este README para ver una versión renderizada y fácil de leer directamente en tu navegador.

2.  **Opción Técnica (GitHub y Entorno Local):**
    * Clona este repositorio: `git clone [URL_DEL_REPOSITORIO]`
    * Asegúrate de tener Python y las librerías necesarias instaladas (pandas, matplotlib, seaborn, jupyter). Puedes crear un entorno virtual:
        ```bash
        python -m venv env
        source env/bin/activate  # En Windows: env\Scripts\activate
        pip install pandas matplotlib seaborn jupyter
        ```
    * Navega a la carpeta del proyecto y ejecuta Jupyter Notebook o JupyterLab:
        ```bash
        jupyter notebook
        # o
        jupyter lab
        ```
    * Abre el archivo `Analisis_inmuebles.ipynb`.

---

