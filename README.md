<h1 align="center"> Challenge2_Telecom-X<h1>
<h2 align="center"> Proposito del análisis<h2>
El proposito del análisis de la base de datos TelecomX_Data.json facilitado por Alura Latam es comprender mediante el tratamiento,estandarización y visualización de los datos el porque de la cancelación de los servicios de la empresa Telecom X.
<h2 align="center"> La estructura del proyecto y organización de los archivos<h2>
<p>La estructura consta de la carga de bibliotecas que se van a utilizar:<p>
<p>import matplotlib.pyplot as plt<p>
<p>import numpy as np<p>
<p>import pandas as pd<p>
<p>import seaborn as sns<p>
<p>Se crean diferentes data frames para cada columna ya que dichas tienen diccionarios en cada una. Esto facilita la extracción de datos y futuras creaciones de visualizaciones.<p>
<p>La verificación del contendido y la estandarización de los datos es necesaria ya que en muchos casos no pueden utilizarse para el desarrollo de las visualizaciones,como por ejemplo los datos en formato string y tienen que ser convertidos a tipo int64.<p>
<h2 align="center"> Visualización de Gráficos<h2>
![image](https://github.com/user-attachments/assets/ae7bf6a7-4f0d-4284-b77c-67a09579acae)
<p>En el gráfico de torta(pie) se observa un importante abandono del servicio, aproximadamente 1/4 del total.</p>
Visualizaciones/visualizacion2.png
<p>En este gráfico de barras(bar) se observa que la diferencia de usuarios(que contraron y tambien los que no continuan con el servicio) es menor. Siendo mayor la cantidad de hombres que contraron el servicio.</p>
Visualizaciones 3
<p>En el siguiente gráfico podemos observar que el abandono del servicio por género sigue siendo menor pero las mujeres son los clientes que más abandonan el servicio por una diferencia menor.</p>
Visualizaciones 4
<p>En el gráfico podemos observar la diferencia de cantidad de usuarios entre los 3 planes (mes a mes, por año y por dos años). Donde tenemos en primer lugar el contrato por mes a mes, en segundo el de dos años y en tercero el anual.</p>
Visualizaciones 5
<p>En el siguiente gráfico podemos observar una difencia notable en cuanto a las bajas de usuarios de distintos planes, el que más evidente es el de mes a mes. Dandonos a entender una incomformidad grave en cuanto al desempeño del servicio.</p>
Visualizaciones 6
<p>En el gráfico se observa una marcada cancelación del servicio por parte de los usuarios mayores de 65 años por sobre el porcentaje de cancelaciones de usuarios menores a dicha edad.</p>
Visualizaciones 7
<p>En este gráfico de barras(bar) se marca una tendecia de abandono de servicio del tipo de fibra optica. Mucho menor en el caso de la DSL y de la linea telefónica.</p>
Visualizaciones 8
<p>En el gráfico de caja(boxplot) podemos observar el gasto total de los clientes que continuan y los que abandonaron el servicio siendo el de abandono menor al gasto de los que continuan. Cabe aclarar que varios clientes que abandonaron hicieron un gasto superior a los clientes activos.</p>
Visualizaciones 9
<p>En el gráfico de caja(boxplot) podemos observar el gasto mensual de los clientes que continuan y los que abandonaron el servicio siendo el de abandono mayor al gasto de los que continuan.</p>
Visualizaciones 10
<p>En el gráfico de barras horizontales(barplot) podemos observar una diferencia muy marcada de abandono de clientes que utilizan el metodo de pago por Electronic check comparado con los otros 3 metodos. Siendo mas de la mitad de los clientes que abandonan.</p>

