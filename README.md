# Analisis_de_consumo_plataforma_en_linea

## 📜 Descripción del Proyecto

Este proyecto consiste en un análisis exploratorio de datos (EDA) sobre un conjunto de datos modificado de Instacart, una plataforma de entrega de comestibles. El objetivo principal es analizar los patrones de compra de los clientes para obtener insights sobre su comportamiento.

A través de la limpieza, preprocesamiento y visualización de datos, se responden preguntas clave como:
- ¿Cuáles son las horas y días de mayor volumen de pedidos?
- ¿Con qué frecuencia compran los clientes?
- ¿Qué productos son los más populares y cuáles se vuelven a pedir con más frecuencia?
- ¿Cómo se componen los carritos de compra?

## 🚀 Análisis Realizado

El proceso de análisis se dividió en tres pasos fundamentales:

1.  **Descripción y Carga de Datos**:
    * Se cargaron 5 conjuntos de datos (`orders`, `products`, `aisles`, `departments`, `order_products`).
    * Se realizó una inspección inicial para entender la estructura, tipos de datos y contenido de cada tabla.

2.  **Preprocesamiento de Datos**:
    * **Manejo de Duplicados**: Se identificaron y eliminaron registros duplicados en los dataframes de órdenes y productos para garantizar la integridad del análisis.
    * **Tratamiento de Valores Ausentes**: Se analizaron y corrigieron los valores nulos en columnas críticas como `days_since_prior_order` (imputados lógicamente, ya que los nulos correspondían al primer pedido de un cliente) y `product_name` (reemplazados por 'Unknown').
    * **Corrección de Tipos de Datos**: Se ajustaron los tipos de datos de varias columnas para optimizar el uso de memoria y la compatibilidad en las operaciones.

3.  **Análisis Exploratorio de Datos (EDA)**:
    * Se crearon visualizaciones (gráficos de barras e histogramas) para analizar la distribución de pedidos por hora del día y día de la semana.
    * Se identificaron los 20 productos más vendidos y los 20 más reordenados.
    * Se calculó la tasa de reorden por producto y por cliente para medir la lealtad.
    * Se analizó qué productos son los primeros en ser añadidos al carrito, como un indicador de su importancia para el consumidor.

## 📊 Conclusiones Clave

El análisis reveló un perfil de consumidor recurrente y con hábitos de compra bien definidos:
* **Horas Pico**: La mayor actividad de compra se concentra entre las **9:00 a.m. y las 3:00 p.m.**
* **Días de Mayor Demanda**: Los **domingos y lunes** son los días con mayor volumen de pedidos, sugiriendo una planificación semanal de las compras.
* **Fidelidad del Cliente**: El 49% de los productos en las órdenes de un cliente promedio son artículos que ya había comprado antes, lo que indica un alto nivel de lealtad.
* **Preferencia por lo Orgánico**: Los productos orgánicos, especialmente frutas y verduras, dominan las listas de los más vendidos y más reordenados, marcando una clara tendencia hacia el consumo saludable.
* **Productos Ancla**: El "Banana" no solo es el producto más vendido, sino también el que con más frecuencia se añade primero al carrito, actuando como un producto de alta recordación para iniciar la compra.

## 💻 Tecnologías Utilizadas

* **Lenguaje**: Python 3
* **Librerías**:
    * `Pandas`: Para la manipulación y análisis de los datos.
    * `NumPy`: Para operaciones numéricas eficientes.
    * `Matplotlib`: Para la generación de gráficos y visualizaciones.

