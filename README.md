Análisis de Rendimiento de Tiendas Alura Store
Este repositorio contiene el código y los resultados de un análisis de datos preliminar para las cuatro sucursales de la cadena Alura Store. El objetivo principal de este proyecto es evaluar el rendimiento de cada tienda, identificar la menos eficiente y generar una recomendación basada en los datos para el Sr. Juan, quien busca desinvertir en una de las tiendas para financiar un nuevo emprendimiento.

**🚀 Objetivo del Proyecto**
El Sr. Juan ha solicitado una evaluación exhaustiva de las cuatro sucursales de su cadena, Alura Store, con el fin de determinar cuál de ellas debería ser desinvertida para financiar un nuevo proyecto empresarial. Para cumplir con este requerimiento, se ha realizado un análisis detallado de los datos de ventas, el rendimiento operativo y las reseñas de clientes correspondientes a cada una de las cuatro tiendas. El propósito fundamental de este estudio es identificar la sucursal con el rendimiento más bajo o la menor eficiencia, y posteriormente formular una recomendación fundamentada en los hallazgos derivados del análisis de los datos.

**📊 Metodología y Análisis**
El análisis se llevó a cabo utilizando Python, aprovechando la potencia de la librería pandas para la manipulación y el análisis de datos, requests para la descarga de los datasets desde URLs, y matplotlib.pyplot (implícitamente para los gráficos si se generaron con Python) para la visualización.

Los pasos principales del análisis fueron:

Carga de Datos: Se cargaron los datos de ventas de las cuatro tiendas (tienda.csv, tienda2.csv, tienda3.csv, tienda4.csv) directamente desde URLs de GitHub, utilizando pandas.read_csv().

Cálculo de Ingresos Totales por Tienda:

Se sumaron los valores de la columna 'Precio' para cada DataFrame para estimar los ingresos totales de cada tienda.
Código Python utilizado: df['Precio'].sum()
Resultado Visual:
Análisis de Cantidad de Productos Vendidos por Categoría:

Se agruparon los datos por 'Categoría de Producto' y se contó el número de ventas para cada tipo, identificando las categorías más populares en cada tienda.
Código Python utilizado: df['Categoría de Producto'].value_counts()
Resultado Visual (Distribución Porcentual):
Cálculo del Envío Promedio por Tienda:

Se calculó el promedio de la columna 'Costo de envío' para cada tienda. Se implementó una robusta gestión de errores con pd.to_numeric(errors='coerce') para manejar valores no numéricos y asegurar la precisión del cálculo.
Código Python utilizado: df['Costo de envío'].mean() (con manejo de tipos de datos).
Resultado en consola:
El Envío promedio de la Tienda N°1 es: 26018.61
El Envío promedio de la Tienda N°2 es: 25216.24
El Envío promedio de la Tienda N°3 es: 24805.68
El Envío promedio de la Tienda N°4 es: 23459.46
Análisis de Calificación Promedio por Tienda:

Se calculó la calificación promedio, indicando el nivel de satisfacción percibido.
Código Python utilizado: Similar a los promedios anteriores sobre la columna 'Calificación'.
Resultado en consola:
La Calificación de la Tienda 1 es: 3.98 ⋆
La Calificación de la Tienda 2 es: 4.04 ⋆
La Calificación de la Tienda 3 es: 4.05 ⋆
La Calificación de la Tienda 4 es: 4.00 ⋆
Identificación de Productos Más Caros y Baratos por Tienda:

Se extrajeron los 10 productos con los precios más altos y los 10 con los precios más bajos para cada tienda.
Código Python utilizado: Métodos de ordenamiento y selección en DataFrames de Pandas.
💡 Conclusión y Recomendación
Basado en el análisis de ingresos totales, volumen de ventas por categoría, calificaciones promedio y costos de envío promedio, la Tienda 4 emerge como la principal candidata para la desinversión. Presenta consistentemente los ingresos totales más bajos y la menor contribución porcentual al ingreso global de la cadena.

Si bien la Tienda 4 muestra los costos de envío promedio más bajos, esta eficiencia logística no compensa su menor rendimiento en ingresos. La Tienda 1, por otro lado, es la líder en ingresos, aunque tiene el costo de envío promedio más alto.


🛠️ Tecnologías Utilizadas
Python 3.x
Pandas: Para manipulación y análisis de datos.
Requests: Para la descarga de datos desde URLs.
io (StringIO): Para manejar datos descargados como archivos en memoria.
