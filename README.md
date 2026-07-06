# Dashboard del coste de la vivienda en Madrid
Dashboard interactivo en Power BI que analiza el coste de la vivienda por distrito en Madrid, cruzando precio y renta para medir el esfuerzo real de acceso.

# El coste de la vivienda en Madrid - Dashboard en Power BI
 
Dashboard interactivo que analiza el coste de acceso a la vivienda en los 21 distritos
de Madrid, cruzando el **precio de la vivienda** con la **renta de los hogares** para
calcular cuántos años de sueldo íntegro cuesta comprar un piso en cada distrito.
 
## ¿Por qué este proyecto?
 
Como joven que se enfrenta al mercado inmobiliario, quise ver con datos reales lo que
todos intuimos: que comprar una vivienda en Madrid se ha vuelto extremadamente difícil.
En lugar de basarme únicamente en una percepción general, construí un análisis que lo mide distrito por
distrito y que permite simular distintos niveles de salario.
 
## Los datos
 
Fuentes públicas del Ayuntamiento de Madrid y del INE:
 
- **Precio de la vivienda por distrito (€/m²)** — Ayuntamiento de Madrid. Años 2023 y 2025. Precio de oferta (valor anunciado), calculado como media de los doce meses de cada año.
- **Renta media por hogar por distrito** — INE, Atlas de Distribución de Renta de los Hogares (ADRH). Año 2023.
- **Supuesto de cálculo:** vivienda tipo de 80 m².
 
**Nota metodológica: El cálculo del esfuerzo de acceso utiliza precios de la vivienda y renta del hogar del mismo año (2023) para garantizar la comparabilidad de los datos. Los precios de 2025 se emplean únicamente en el análisis de la evolución del mercado inmobiliario, ya que no existen datos de renta del hogar igualmente actualizados.
 
**Nota sobre el tipo de precio:** se trata de precios de oferta (lo que se pide en los anuncios), no de precios de transacción cerrada. Reflejan correctamente la tendencia y las diferencias entre distritos, si bien el precio real de las operaciones puede ser algo inferior.
 
## Técnicas aplicadas
 
- **Power Query** - limpieza y transformación de dos fuentes de datos crudas.
- **Modelado de datos** - relación entre las tablas de precio y renta a través del campo
  común (distrito).
- **DAX** - medidas y columnas calculadas para el precio de un piso de 80 m², el esfuerzo de acceso (años de sueldo), el incremento porcentual de precios 2023-2025 y los valores agregados de las tarjetas (media, máximo y mínimo).
- **Parámetro interactivo** - un control deslizante (slider) que permite simular distintos
  salarios anuales y ver cómo cambia el esfuerzo de acceso en tiempo real.
- **Diseño del dashboard** - tarjetas KPI, gráficos comparativos, tabla de detalle y
  formato condicional.
 
## Estructura del dashboard
 
### Página 1 — Accesibilidad (¿cuánto cuesta acceder a una vivienda?)
Tarjetas KPI, años de sueldo según renta del hogar, años de sueldo según el salario seleccionado en el deslizador, y tabla de detalle por distrito. Datos de 2023.
 
### Página 2 — Evolución de precios (¿cuánto ha subido la vivienda? 2023-2025)
Subida del precio por distrito en porcentaje (ordenada de mayor a menor) y comparativa de precio por m² entre 2023 y 2025.
 
## Qué se descubre
 
**Sobre la accesibilidad (2023):**
 
- El esfuerzo de acceso más alto según renta del hogar está en el **Centro**, seguido de **Salamanca** y **Chamberí**.
- **Salamanca** tiene la vivienda más cara, pero no la renta más alta — esa es **Chamartín**. El precio del metro cuadrado no refleja necesariamente el poder adquisitivo de quien vive en el distrito.
- Con un salario joven de 21.000 €, comprar un piso de 80 m² supera de media los **14 años de sueldo íntegro**, y eso dedicando el 100 % del salario sin gastar en nada más. En la práctica, inalcanzable.
**Sobre la evolución de precios (2023-2025):**
 
- El precio de la vivienda ha subido en **todos los distritos sin excepción**, con incrementos que van aproximadamente del **30 % al 50 % en solo dos años**.
- Las subidas más pronunciadas no están en los distritos más caros, sino en algunos de los **más asequibles** (como Usera y Moratalaz). Esto reduce la oferta de vivienda económica y presiona a los hogares con menor poder adquisitivo.
- El dato más preocupante surge al comparar con los ingresos: mientras los precios crecieron entre un 30 % y un 50 %, la renta de los hogares aumentó en torno a un 7 % anual (~14 % en el periodo). **La vivienda se ha encarecido a un ritmo dos o tres veces superior al de los salarios**, lo que agrava el esfuerzo de acceso año tras año.
## Herramientas
 
`Power BI` · `Power Query (M)` · `DAX` · `Modelado de datos` · Datos abiertos del Ayuntamiento de Madrid · INE (Atlas de Distribución de Renta de los Hogares)
 
## Contenido del repositorio
 
- `dashboard-vivienda-madrid.pbix` - el archivo de Power BI.
- `dashboard.png` - captura del dashboard.
- `datos/` - los archivos de datos utilizados (precio y renta).
---
 
*Autora: Irene Jurado Castillo*
