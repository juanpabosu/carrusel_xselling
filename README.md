# Data Engineering - Carrusel de Venta Cruzada  
Un carrusel de venta cruzada es un elemento de la interfaz de usuario, que suele encontrarse en los sitios web de comercio electrónico, que muestra productos relacionados o complementarios en un formato desplazable horizontalmente, incentivando a los usuarios a comprar artículos adicionales junto a su selección actual. Este método ayuda a aumentar el valor medio de los pedidos y mejora la experiencia general de compra al sugerir productos relevantes de forma atractiva y visualmente atractiva.

En esencia, los carruseles de venta cruzada son una herramienta estratégica para que las empresas de comercio electrónico impulsen las ventas y mejoren el recorrido del cliente aprovechando el poder de las recomendaciones de productos.

## Descripcion del enunciado

En el contexto de MercadoPago, se quiere desarrollar un modelo de Machine Learning para predecir el orden de un conjunto de Propuestas de Valor (aka, Value Props) en el carrusel de la app llamado “Descubrí Más”.

<div align="center">
 <img src="https://github.com/user-attachments/assets/af938d45-4fa8-465c-8898-76a9445bda84">
</div>  

La tarea consiste en construir un pipeline utilizando Python y sus librerías, que tenga como input 3 fuentes de datos diferentes y genere como resultado un dataset listo para ser ingerido por el modelo.   

**Data Sources**  
- Prints (prints.json) - historial de 1 mes de value props que fueron mostradas a cada usuario, en formato json lines
- Taps (taps.json) - historial de 1 mes de value props que fueron clickeadas por un usuario, en formato json lines 
- Payments (pays.csv) - historial de 1 mes de pagos realizados por los usuarios, en formato csv
 
**Resultado esperado**  

El dataset a construir deberá contar con la siguiente información:  

-   prints de la última semana
-   por cada print:
    -   un campo que indique si se hizo click o no 
    -   cantidad de veces que el usuario vio cada value prop en las 3 semanas previas a ese print.
    -   cantidad de veces que el usuario clickeo cada value prop en las 3 semanas previas a ese print.
    -   cantidad de pagos que el usuario realizó para cada value prop en las 3 semanas previas a ese print.
    -   importes acumulados que el usuario gasto para cada value prop en las 3 semanas previas a ese print.
 
**Estructura del repositorio**

**data**: contiene los set de datos originales y el dataset de salida

**src**: código fuente y salidas del proyecto en formato .ipynb.
