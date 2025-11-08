# Análisis de Transacciones de Tiendas en Colombia

Este proyecto consiste en un análisis exploratorio de datos (EDA) sobre transacciones de cuatro tiendas en Colombia, con el objetivo de identificar patrones, evaluar el rendimiento de cada tienda y proporcionar recomendaciones basadas en los hallazgos.

## 📊 Conjunto de Datos

El análisis se basó en datos de transacciones recopilados de cuatro tiendas diferentes. Cada conjunto de datos de tienda (`tienda_1.csv`, `tienda_2.csv`, `tienda_3.csv`, `tienda_4.csv`) contiene información detallada sobre cada venta, incluyendo:

*   **Producto:** Nombre del producto vendido.
*   **Categoría del Producto:** Categoría a la que pertenece el producto.
*   **Precio:** Precio de venta del producto.
*   **Costo de envío:** Costo asociado al envío del producto.
*   **Fecha de Compra:** Fecha en que se realizó la transacción.
*   **Vendedor:** Nombre del vendedor que realizó la venta.
*   **Lugar de Compra:** Ciudad donde se realizó la compra.
*   **Calificación:** Calificación otorgada por el cliente a la transacción/producto (1-5 estrellas).
*   **Método de pago:** Método utilizado para pagar la compra.
*   **Cantidad de cuotas:** Número de cuotas si el pago fue a crédito.
*   **lat / lon:** Coordenadas geográficas de la ubicación de la transacción.
*   **No_tienda:** Identificador de la tienda (agregado durante el preprocesamiento).
*   **Ganancia Neta:** Calculado como `Precio - Costo de envío`.

Los datos fueron consolidados en un único DataFrame para facilitar el análisis comparativo.

## 🔬 Análisis Realizados

Se llevaron a cabo los siguientes análisis clave:

1.  **Facturación Total por Tienda:** Comparación del total facturado por cada una de las cuatro tiendas.
2.  **Ventas por Categoría:** Análisis de las categorías de productos que generan mayores ventas en cada tienda individual.
3.  **Calificación Promedio por Tienda:** Evaluación de la satisfacción del cliente en cada tienda mediante la calificación promedio.
4.  **Productos Más y Menos Vendidos:** Identificación de los productos más rentables y los más populares (o impopulares) en cada tienda.
5.  **Costo de Envío Promedio por Tienda:** Comparación de los costos de envío promedio incurridos por cada tienda.
6.  **Ganancia Neta por Tienda:** Cálculo y comparación de la ganancia neta total de cada tienda.
7.  **Ubicación Geográfica de Transacciones:** Visualización interactiva de la distribución geográfica de las transacciones para todas las tiendas en Colombia, utilizando `plotly.express`.

## 📈 Conclusiones Clave y Recomendaciones

A partir del análisis, se obtuvieron las siguientes conclusiones y se formularon recomendaciones:

*   **Facturación y Ganancia Neta:** La **Tienda 1** consistentemente se posiciona como la de mayor facturación y ganancia neta total, seguida de cerca por la Tienda 2. La **Tienda 4** muestra la menor ganancia neta.
*   **Calificación de Clientes:** La **Tienda 3** y la **Tienda 2** tienen las calificaciones promedio más altas, mientras que la **Tienda 1** y la **Tienda 4** tienen las más bajas, aunque todas las tiendas mantienen calificaciones por encima de 3.9.
*   **Costo de Envío:** La **Tienda 1** presenta el costo de envío promedio más alto, lo cual, a pesar de su alta ganancia, sugiere oportunidades para optimizar la logística. La **Tienda 4** tiene el costo de envío más bajo.
*   **Distribución Geográfica:** El mapa interactivo revela que todas las tiendas tienen una fuerte concentración de ventas en las principales ciudades de Colombia (Bogotá, Medellín, Cali). Se observan ligeras variaciones en la cobertura, con la Tienda 3 mostrando presencia en la costa caribeña y la Tienda 4 en ciudades como Cúcuta.
*   **Productos por Categoría:** Las categorías de productos con mayor facturación varían ligeramente entre tiendas, pero "Muebles" y "Electrónicos" suelen ser categorías de alto rendimiento.

**Recomendación Específica:**

Considerando la combinación de la **menor ganancia neta total** y una de las **calificaciones promedio más bajas**, se sugiere **revaluar la operación de la Tienda 4**. Aunque su costo de envío es bajo, este no compensa su menor rentabilidad y satisfacción del cliente relativa. Se recomienda investigar a fondo las causas de su bajo rendimiento (ej. ubicación, gestión, competencia local, estrategias de marketing) antes de tomar decisiones drásticas como un posible cierre, o para implementar mejoras dirigidas.

## 🛠️ Herramientas

*   **Lenguaje de Programación:** Python
*   **Librerías Principales:**
    *   `pandas` para manipulación y análisis de datos.
    *   `matplotlib.pyplot` para visualizaciones estáticas.
    *   `seaborn` para visualizaciones estadísticas mejoradas.
    *   `plotly.express` para visualizaciones interactivas (mapas).
