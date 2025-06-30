
<h1 align="center"> Challenge2_Telecom-X<h1>
  
<h2 align="center">📊 Proposito del análisis<h2>    
El proposito del análisis de la base de datos TelecomX_Data.json facilitado por Alura Latam es comprender mediante el tratamiento,estandarización y visualización de los datos el porque de la cancelación de los servicios de la empresa Telecom X.
<h2 align="center">📝La estructura del proyecto y organización de los archivos<h2>
<p>La estructura consta de la carga de bibliotecas que se van a utilizar:<p>
<p>import matplotlib.pyplot as plt<p>
<p>import numpy as np<p>
<p>import pandas as pd<p>
<p>import seaborn as sns<p>
<p>Se crean diferentes data frames para cada columna ya que dichas tienen diccionarios en cada una. Esto facilita la extracción de datos y futuras creaciones de visualizaciones.<p>
<p>La verificación del contendido y la estandarización de los datos es necesaria ya que en muchos casos no pueden utilizarse para el desarrollo de las visualizaciones,como por ejemplo los datos en formato string y tienen que ser convertidos a tipo int64.<p>
<h2 align="center">📈Visualización de Gráficos<h2>
<div align="center">
<img src="https://i.postimg.cc/52fvNStQ/visualizacion1.jpg" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, obtiene el recuento de clientes que abandonaron ('Sí') y los que no ('No') de la columna Churn de tu DataFrame df_final y los almacena en la variable churn_counts.
Luego, crea una figura y ejes para el gráfico con un fondo gris claro.
Finalmente, genera el gráfico de pastel utilizando los datos de churn_counts. El argumento labels proporciona etiquetas descriptivas para cada porción, incluyendo los recuentos reales. autopct formatea el porcentaje mostrado en cada porción a un decimal, y startangle rota el punto de inicio de la primera porción. El argumento colors establece los colores para las porciones. Se establece el título del gráfico y plt.show() muestra el gráfico de pastel generado.</p>
<p>Análisis:En el gráfico de torta(pie) se observa un importante abandono del servicio, aproximadamente 1/4 del total.</p>
<div align="center">
<img src="https://i.postimg.cc/kGtzjtRq/visualizacion2.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, utiliza value_counts() en la columna gender del DataFrame df_final para obtener el recuento de cada género. El resultado se guarda en la variable genrer_count.
Primero, crea una figura para el gráfico con un tamaño específico y un color de fondo gris claro.
Luego, crea el gráfico de barras utilizando los índices (género) y los valores (cantidad de clientes) de genrer_count. Se establecen las etiquetas de los ejes x e y, y el título del gráfico.
Finalmente, añade etiquetas de texto encima de cada barra para mostrar la cantidad exacta de clientes por género y muestra el gráfico.</p>
<p>Análisis:En este gráfico de barras(bar) se observa que la diferencia de usuarios(que contraron y tambien los que no continuan con el servicio) es menor. Siendo mayor la cantidad de hombres que contraron el servicio.</p>
<div align="center">
<img src="https://i.postimg.cc/mDrtFTzQ/visualizacion3.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Este código filtra el DataFrame df_final para obtener solo las filas donde la columna 'Churn' es igual a 1 (indicando que el cliente abandonó el servicio). El resultado se almacena en un nuevo DataFrame llamado churned_customers. Luego, cuenta la cantidad de clientes que abandonaron para cada género en el DataFrame churned_customers y guarda los resultados en la variable churn_gender_counts.Este código genera un gráfico de barras para visualizar la distribución de clientes que abandonaron el servicio, diferenciados por género.
Comienza creando una figura con un tamaño específico y un color de fondo gris claro.
Luego, crea el gráfico de barras utilizando los índices (género) y los valores (cantidad de clientes que abandonaron) de churn_gender_counts. Se establecen las etiquetas de los ejes x e y, y el título del gráfico.
Finalmente, añade etiquetas de texto encima de cada barra para mostrar la cantidad exacta de clientes que abandonaron por género y muestra el gráfico.</p>
<p>Análisis:En el siguiente gráfico podemos observar que el abandono del servicio por género sigue siendo menor pero las mujeres son los clientes que más abandonan el servicio por una diferencia menor.</p>
<div align="center">
<img src="https://i.postimg.cc/RZQ7XKCK/visualizacion4.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Utiliza value_counts() en la columna Contract del DataFrame account para obtener el recuento de cada tipo de contrato. El resultado se guarda en la variable contract.Primero, crea una figura para el gráfico con un tamaño específico y un color de fondo gris claro.
Luego, genera el gráfico de pastel utilizando los valores de contract. Los labels del gráfico de pastel son los índices de contract (los tipos de contrato). autopct formatea el porcentaje mostrado en cada porción a un decimal, y startangle rota el punto de inicio de la primera porción. Se utiliza sns.color_palette para obtener una paleta de colores para las porciones. Se establece el título del gráfico y se alinea a la derecha. Finalmente, plt.show() muestra el gráfico de pastel generado.</p>
<p>Análisis:En el gráfico podemos observar la diferencia de cantidad de usuarios entre los 3 planes (mes a mes, por año y por dos años). Donde tenemos en primer lugar el contrato por mes a mes, en segundo el de dos años y en tercero el anual.</p>
<div align="center">
<img src="https://i.postimg.cc/DzkNbqjG/visualizacion5.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, agrupa el DataFrame df_final por la columna 'Contract' y luego cuenta los valores de 'Churn' dentro de cada grupo. normalize=True calcula los porcentajes, y unstack() remodela el resultado para tener los tipos de contrato como filas y los valores de 'Churn' (0 y 1) como columnas.
Luego, imprime el DataFrame resultante (churn_by_contract) que muestra el porcentaje de abandono para cada tipo de contrato.
Después, crea una figura para el gráfico con un color de fondo gris claro.
A continuación, genera un gráfico de barras a partir del DataFrame churn_by_contract para visualizar los porcentajes de abandono por tipo de contrato. Se establecen el título, las etiquetas de los ejes y la leyenda. Las etiquetas del eje x se rotan a 0 grados para mayor legibilidad.
Finalmente, añade etiquetas de texto encima de cada barra para mostrar el porcentaje exacto de abandono y muestra el gráfico.</p>
<p>Análisis:En el siguiente gráfico podemos observar una difencia notable en cuanto a las bajas de usuarios de distintos planes, el que más evidente es el de mes a mes. Dandonos a entender una incomformidad grave en cuanto al desempeño del servicio.</p>
<div align="center">
<img src="https://i.postimg.cc/ydqSKNNs/visualizacion6.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:rimero, agrupa el DataFrame df_final por la columna 'SeniorCitizen' y luego cuenta los valores de 'Churn' dentro de cada grupo. normalize=True calcula los porcentajes, y unstack() remodela el resultado para tener las categorías de edad (0 y 1) como filas y los valores de 'Churn' (0 y 1) como columnas.
Luego, imprime el DataFrame resultante (señior_churn) que muestra el porcentaje de abandono para cada categoría de edad.
Después, crea una figura para el gráfico con un color de fondo gris claro.
A continuación, genera un gráfico de barras a partir del DataFrame señior_churn para visualizar los porcentajes de abandono por categoría de edad. Se establecen el título, las etiquetas de los ejes y la leyenda. Las etiquetas del eje x se personalizan para mostrar "Menor de 65 años" y "Mayor de 65 años".Finalmente, añade etiquetas de texto encima de cada barra para mostrar el porcentaje exacto de abandono y muestra el gráfico.</p>
<p>Análisis:En el gráfico se observa una marcada cancelación del servicio por parte de los usuarios mayores de 65 años por sobre el porcentaje de cancelaciones de usuarios menores a dicha edad.</p>
<div align="center">
<img src="https://i.postimg.cc/bJ8NLSJD/visualizacion7.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, agrupa el DataFrame df_final por la columna 'InternetService' y luego cuenta los valores de 'Churn' dentro de cada grupo. normalize=True calcula los porcentajes, y unstack() remodela el resultado para tener los tipos de servicio de Internet como filas y los valores de 'Churn' (0 y 1) como columnas.
Luego, imprime el DataFrame resultante (Internet_Service_churn) que muestra el porcentaje de abandono para cada tipo de servicio de Internet.
Después, crea una figura para el gráfico con un color de fondo gris claro.
A continuación, genera un gráfico de barras a partir del DataFrame Internet_Service_churn para visualizar los porcentajes de abandono por tipo de servicio de Internet. Se establecen el título, las etiquetas de los ejes y la leyenda. Las etiquetas del eje x se personalizan para mostrar "DSL", "Fibra óptica" y "Solo línea telefónica".Finalmente, añade etiquetas de texto encima de cada barra para mostrar el porcentaje exacto de abandono y muestra el gráfico.</p>
<p>Análisis:En este gráfico de barras(bar) se marca una tendecia de abandono de servicio del tipo de fibra optica. Mucho menor en el caso de la DSL y de la linea telefónica.</p>
<div align="center">
<img src="https://i.postimg.cc/Bbz3WjqC/visualizacion8.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, crea una figura para el gráfico con un tamaño específico y un color de fondo gris claro.
Luego, utiliza seaborn.boxplot para crear el gráfico. El eje x representa si el cliente abandonó (0 para No, 1 para Sí), el eje y representa los cargos totales, y los datos provienen de df_final. Se utiliza una paleta de colores específica.
Se establecen el título del gráfico, las etiquetas de los ejes x e y. Las etiquetas del eje x se personalizan para mostrar "No Abandonó" y "Abandonó".Finalmente, plt.show() muestra el gráfico de caja generado.</p>
<p>Análisis:En el gráfico de caja(boxplot) podemos observar el gasto total de los clientes que continuan y los que abandonaron el servicio siendo el de abandono menor al gasto de los que continuan. Cabe aclarar que varios clientes que abandonaron hicieron un gasto superior a los clientes activos.</p>
<div align="center">
<img src="https://i.postimg.cc/TwYvpV19/visualizacion9.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Primero, crea una figura para el gráfico con un tamaño específico y un color de fondo gris claro.
Luego, utiliza seaborn.boxplot para crear el gráfico. El eje x representa si el cliente abandonó (0 para No, 1 para Sí), el eje y representa los cargos mensuales, y los datos provienen de df_final. Se utiliza una paleta de colores específica.
Se establecen el título del gráfico, las etiquetas de los ejes x e y. Las etiquetas del eje x se personalizan para mostrar "No Abandonó" y "Abandonó".
Finalmente, plt.show() muestra el gráfico de caja generado.
<p>Análisis:En el gráfico de caja(boxplot) podemos observar el gasto mensual de los clientes que continuan y los que abandonaron el servicio siendo el de abandono mayor al gasto de los que continuan.</p>
<div align="center">
<img src="https://i.postimg.cc/0QWRmzJq/visualizacion10.png" style="max-width: 80%; border: 1px solid #ddd; border-radius: 4px; padding: 5px; background: white;">
</div>
<p>Desarrollo:Este código calcula la cantidad y el porcentaje de clientes que abandonaron el servicio, agrupados por el método de pago, y luego visualiza estos porcentajes en un gráfico de barras horizontales.
Primero, filtra el DataFrame df_final para obtener solo los clientes que abandonaron ('Churn' == 1) y los almacena en churned_customers.
Luego, cuenta la frecuencia de cada método de pago dentro de churned_customers y lo guarda en churn_by_payment_method.Calcula el total de clientes que abandonaron y luego calcula el porcentaje de abandono para cada método de pago dividiendo la cantidad de abandonos por método de pago entre el total de abandonos.Crea un nuevo DataFrame (churn_payment_df) para organizar estos recuentos y porcentajes.Imprime el DataFrame churn_payment_df.Crea una figura para el gráfico con un tamaño específico y un color de fondo gris claro.Genera un gráfico de barras horizontales utilizando el porcentaje de abandono en el eje x y los métodos de pago en el eje y.Establece el título del gráfico y las etiquetas de los ejes.
Finalmente, añade etiquetas de texto al final de cada barra para mostrar el porcentaje exacto de abandono y muestra el gráfico.</p>
<p>Análisis:En el gráfico de barras horizontales(barplot) podemos observar una diferencia muy marcada de abandono de clientes que utilizan el metodo de pago por Electronic check comparado con los otros 3 metodos. Siendo mas de la mitad de los clientes que abandonan.</p>
<h2 align="center">📌Conclusión<h2>
<p>🔍Alta tasa de abandono general
El 26.5% de los clientes abandonan el servicio (1 de cada 4), lo que representa un problema crítico de retención.
Mayores de 65 años tienen una tasa de churn significativamente mayor que los más jóvenes.
Mujeres abandonan ligeramente más que los hombres.
Los clientes con contrato "mes a mes" son los que más abandonan (representan casi el 50% del churn total).
La fibra óptica muestra la mayor tasa de abandono entre los servicios de internet (posiblemente por expectativas no cumplidas o problemas técnicos).
Factores financieros
Los clientes que abandonan tienen cargos mensuales más altos (pero un gasto total acumulado menor), sugiriendo que perciben poco valor por el precio.
El método de pago "Electronic Check" está asociado con mas del 50% de las cancelaciones (posibles problemas de usabilidad o falta de recordatorios automáticos).
<p>🚨 Posibles Causas Raíz
Insatisfacción con planes "mes a mes": Flexibilidad que permite salidas fáciles, pero quizá falta de beneficios para retener.
Problemas con fibra óptica: Velocidad inestable, soporte técnico deficiente o precios no competitivos.
Experiencia de clientes mayores: Dificultad con plataformas digitales o falta de atención personalizada.
Fricción en pagos: El "Electronic Check" puede requerir demasiados pasos manuales comparado con opciones automáticas.</p>
<p>💡 Posibles Soluciones
Mejorar contratos "mes a mes"
Ofrecer descuentos por fidelidad o beneficios progresivos (ej: "3 meses continuos = upgrade gratis").
Mejorar la fibra óptica
Revisar calidad del servicio, tiempos de respuesta a fallas y comunicación transparente sobre limitaciones.
Programa para adultos mayores
Soporte telefónico dedicado o talleres de uso de plataformas.
Incentivar pagos automáticos(ej:descuentos por su uso)</p>
<p>🎯Conclusión final: Telecom X tiene oportunidades claras para reducir el churn enfocándose en experiencia del cliente, flexibilidad de contratos y simplificación de pagos, especialmente en segmentos críticos (adultos mayores y usuarios de fibra óptica). La data sugiere que pequeñas mejoras en estos puntos podrían reducir significativamente las cancelaciones.</p>
</div>

