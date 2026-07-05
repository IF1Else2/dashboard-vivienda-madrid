# Dashboard del coste de la vivienda en Madrid
Dashboard interactivo en Power BI que analiza el coste de la vivienda por distrito en Madrid, cruzando precio y renta para medir el esfuerzo real de acceso.

# El coste de la vivienda en Madrid — Dashboard en Power BI
 
Dashboard interactivo que analiza el coste de acceso a la vivienda en los 21 distritos
de Madrid, cruzando el **precio de la vivienda** con la **renta de los hogares** para
calcular cuántos años de sueldo íntegro cuesta comprar un piso en cada distrito.
 
## ¿Por qué este proyecto?
 
Como joven que se enfrenta al mercado inmobiliario, quise ver con datos reales lo que
todos intuimos: que comprar una vivienda en Madrid se ha vuelto extremadamente difícil.
En lugar de basarme únicamente en una percepción general, construí un análisis que lo mide distrito por
distrito y que permite simular distintos niveles de salario.
 
## Los datos
 
Fuentes públicas del **Ayuntamiento de Madrid**:
 
- **Precio de la vivienda** por distrito (€/m²) — 2025.
- **Renta media por hogar** por distrito — 2022 (último dato disponible).
**Supuesto de cálculo:** vivienda tipo de **80 m²**.
 
> Nota sobre las fuentes: los datos de precio (2025) y renta (2022) no son del mismo año
> porque las estadísticas públicas se actualizan a distinto ritmo. Se usaron los datos más
> recientes disponibles de cada una, y esta limitación se declara explícitamente en el
> propio dashboard.
 
## Técnicas aplicadas
 
- **Power Query** — limpieza y transformación de dos fuentes de datos crudas.
- **Modelado de datos** — relación entre las tablas de precio y renta a través del campo
  común (distrito).
- **DAX** — medidas calculadas para el precio de un piso de 80 m², el esfuerzo de acceso
  (años de sueldo) y los valores agregados de las tarjetas (media, máximo y mínimo).
- **Parámetro interactivo** — un control deslizante (slider) que permite simular distintos
  salarios anuales y ver cómo cambia el esfuerzo de acceso en tiempo real.
- **Diseño del dashboard** — tarjetas KPI, gráficos comparativos, tabla de detalle y
  formato condicional.
 
## Qué se descubre
 
- **El esfuerzo de acceso más alto (según renta del hogar) está en el Centro**, seguido de
  Salamanca y Chamberí.
- **Salamanca tiene la vivienda más cara, pero no la renta más alta** — esa es Chamartín.
  El precio del metro cuadrado no refleja necesariamente el poder adquisitivo de quien vive
  en el distrito.
- **Con un salario joven de 21.000 €**, comprar un piso de 80 m² supera de media los
  **19 años de sueldo íntegro** — y eso dedicando el 100 % del salario, sin gastar en nada
  más. En la práctica, inalcanzable.
## Herramientas
 
`Power BI` · `Power Query (M)` · `DAX` · `Modelado de datos` · Datos abiertos del Ayuntamiento de Madrid
 
## Contenido del repositorio
 
- `dashboard-vivienda-madrid.pbix` — el archivo de Power BI.
- `dashboard.png` — captura del dashboard.
- `dashboard.pdf` — versión en PDF.
- `datos/` — los archivos de datos utilizados (precio y renta).
---
 
*Autora: Irene Jurado Castillo*
