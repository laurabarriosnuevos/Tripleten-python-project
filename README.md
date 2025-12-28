# Análisis de Movilidad Urbana y Productividad Económica  
### Banco de Desarrollo de América Latina – Proyecto de Analítica de Datos (Python)

## Descripción del Proyecto
Como analista de datos en el **Banco de Desarrollo de América Latina**, este proyecto tiene como objetivo comprender la relación entre la **movilidad urbana** (congestión vial, retrasos y tiempos de viaje) y la **productividad económica** (PIB per cápita y desempleo) en las principales ciudades de América Latina.

El propósito es identificar **en qué ciudades se deben priorizar inversiones en infraestructura de transporte** para mejorar la productividad, el desempeño económico y el bienestar general de la población.

Este análisis respalda la toma de decisiones basada en datos para políticas de desarrollo urbano y movilidad en la región.

---

##  Fuentes de Datos
Este proyecto integra dos conjuntos de datos reales:

- **Movilidad Urbana**  
  *TomTom Traffic Index*  
  Proporciona indicadores de tráfico en tiempo real y agregados, como niveles de congestión, retrasos y tiempos de viaje.

- **Economía Urbana**  
  *OECD Cities Database*  
  Incluye datos de PIB per cápita, tasas de desempleo y población por ciudad.

---

##  Preguntas de Negocio
- ¿Qué ciudades de América Latina presentan **alta congestión y baja productividad económica**?
- ¿Cuáles muestran los **mejores indicadores combinados** (movilidad eficiente y economía sólida)?
- ¿Qué variables parecen tener una **relación más fuerte con el desarrollo urbano**?
- ¿Un mayor PIB per cápita implica necesariamente mayor congestión?

---

##  Objetivos de Aprendizaje
Al finalizar este proyecto, se demuestra la capacidad de:

- Crear un **dataset único, limpio y consistente** a partir de múltiples fuentes.
- Aplicar procesos de **limpieza, estandarización y validación de datos**.
- Filtrar y enfocar el análisis en **ciudades latinoamericanas**.
- Calcular **indicadores agregados por ciudad–año**.
- Realizar **análisis exploratorios y validaciones visuales**.
- Documentar todo el proceso analítico en **Jupyter Notebook**.
- Exportar un **dataset final listo para análisis**.

---

##  Metodología

### Preparación de Datos
- Conversión de columnas de fechas desde texto a `datetime64`, manejando valores inválidos y eliminando el sufijo UTC.
- Estandarización de formatos numéricos:
  - Eliminación de separadores de miles.
  - Reemplazo de comas decimales por puntos.
  - Eliminación de símbolos de porcentaje.
  - Conversión de columnas numéricas a tipo `float`.
- Transformación de la población desde millones a valores absolutos.
- Estandarización de los nombres de columnas a formato `snake_case`.

### Estructuración de Datos
- Filtrado de ambos datasets al **año 2024** para garantizar consistencia temporal.
- Agregación de los datos de tráfico por **ciudad–año**, calculando promedios de congestión, retrasos, número de atascos y tiempo de viaje.
- Integración de los datasets mediante una **unión INNER**, asegurando alineación temporal y evitando duplicados.

### Validación y Análisis Exploratorio
- Boxplots para analizar la distribución de los retrasos por congestión e identificar outliers.
- Histogramas para evaluar la distribución del PIB per cápita.
- Gráficos comparativos para observar patrones, tendencias y posibles relaciones entre movilidad y economía.

---

##  Cobertura de Datos
- **Año analizado:** 2024  
- **Ciudades:** 15  
- **Países:** 7 (Sudamérica)

---

##  Principales Hallazgos
- No existe una **relación lineal o directa** entre el PIB per cápita y la congestión vial.
- Un mayor nivel de productividad económica no implica necesariamente mayor congestión.
- Los indicadores de congestión están **fuertemente correlacionados entre sí**, mientras que su relación con las variables económicas es mínima.
- Los tiempos de viaje y retrasos están determinados principalmente por las **condiciones reales del tráfico**, no por el nivel de riqueza de la ciudad.

### Ciudades Críticas Identificadas
- **Santiago** presenta el desbalance más crítico: altos niveles de congestión combinados con un PIB per cápita relativamente bajo, lo que genera una presión desproporcionada sobre la productividad.
- **Bogotá** muestra niveles de congestión aún mayores con un PIB per cápita moderado, lo que la vuelve económicamente vulnerable.
- **Ciudad de México** y **São Paulo** presentan niveles extremadamente altos de congestión, representando oportunidades estratégicas donde las inversiones en movilidad podrían generar retornos significativos.

---

## Recomendaciones de Negocio
- Priorizar **inversiones en infraestructura de movilidad** en Santiago y Bogotá para proteger la productividad económica.
- Implementar **sistemas inteligentes de tráfico**, rediseño de intersecciones y estrategias de gestión de congestión.
- Fortalecer alternativas de **movilidad sostenible**, como transporte masivo y ciclovías seguras.
- En Ciudad de México y São Paulo, grandes inversiones en movilidad podrían generar altos retornos al reducir pérdidas de tiempo y mejorar la eficiencia urbana.

---

## Herramientas y Tecnologías
- Python  
- Pandas y NumPy  
- Matplotlib / Seaborn  
- Jupyter Notebook  



