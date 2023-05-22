# **Pronóstico de la evolución del PIB en las cuatro economías más grandes de Latinoamérica**

Este es un proyecto de ciencia de datos que se enfoca en predecir la evolución del PIB en las cuatro economías más grandes de Latinoamérica: Argentina, Brasil, México y Colombia. Para ello, se utilizan modelos econométricos y estadísticos que permiten analizar la evolución histórica del PIB y proyectar su comportamiento futuro.

## Estructura del proyecto

El proyecto se organiza en los siguientes pasos:

1.	Exploración y análisis de datos: se recopila y procesa la información necesaria sobre el PIB de cada país, se realizan análisis estadísticos y gráficos para entender su evolución histórica y se identifican patrones y tendencias relevantes.
2.	Modelado econométrico: se construyen modelos econométricos basados en series de tiempo para predecir el PIB en cada país. Se utilizan técnicas de regresión y análisis de residuos para evaluar la calidad de los modelos y ajustar sus parámetros.
3.	Validación y comparación de modelos: se comparan los modelos de cada país y se selecciona el que mejor ajusta a los datos históricos. Se realizan pruebas de significancia y se evalúan las predicciones para validar su precisión y confiabilidad.
4.	Proyección del PIB: se utilizan los modelos seleccionados para predecir la evolución futura del PIB en cada país. Se presentan las proyecciones en gráficos y se discuten las implicaciones económicas y políticas de los resultados obtenidos.

## Archivos del proyecto
El proyecto se organiza en los siguientes archivos:
*	datos/gdpe.xls: archivo con los datos históricos del PIB de todos los paises desde 1960 hasta 2021.
*	piblatam.ipynb: archivo Jupyter Notebook con el código Python que implementa los análisis y modelos econométricos del proyecto.
*	README.md: archivo Markdown que describe el proyecto y su estructura.
Requisitos del proyecto


## Exploración y análisis de datos

En la siguiente graficas e mostrata la evolucion del PIB para las principales 4 economias durante el tiempo

![pib_inicial]()

## Modelado econométrico

Se realizan pruebas de estacionariedad para las diferentes economias utilizando de los resultados de los tests, podemos concluir lo siguiente:

1. Tanto el test de Dickey-Fuller aumentado como el test de Phillips-Perron rechazan la hipótesis nula, lo que indica que la serie de tiempo tiene raíz unitaria y necesita ser diferenciada para ser estacionaria.
2. El test KPSS acepta la hipótesis nula, lo que sugiere que el proceso es débilmente estacionario.

Se recomienda aplicar una diferencia de primer orden en la serie de tiempo para lograr la estacionariedad y poder realizar pronósticos más precisos.

Otro metodo para observar la estacionariedad es mediante la grafica PACF y ACF que se muestran a continuacion:

![acf_pacf]()

## Validación y comparación de modelos

Utilizando la funcion auto_arima de la libreria pmdarima observamos que los mejores modelos son:

1. Brasil : SARIMAX(0,1,1)(1,1,0,12)
2. Mexico : SARIMAX(2,1,0)(0,1,1,12)
3. Argentinca : SARIMAX(0,1,1)(0,1,1,12)
4. Colombia : SARIMAX(0,1,1)(1,1,0,12)

## Proyección del PIB

A continuacion se mostrara el resultado de las predicciones para cada pais:

1. Brasil:

![Pib_Brasil](https://github.com/juanguzman2/Pronostico-de-la-evolucion-del-PIB-en-las-cuatro-economias-mas-grandes-de-Latinoamerica/blob/master/Imagenes/PibBrasil.png?raw=true)

2. Mexico:

![PIB_mexico](https://github.com/juanguzman2/Pronostico-de-la-evolucion-del-PIB-en-las-cuatro-economias-mas-grandes-de-Latinoamerica/blob/master/Imagenes/PibMexico.png?raw=true)

3. Argentina

![PIB_argentina](https://github.com/juanguzman2/Pronostico-de-la-evolucion-del-PIB-en-las-cuatro-economias-mas-grandes-de-Latinoamerica/blob/master/Imagenes/PibArgentina.png?raw=true)

4. Colombia

![PIB_Colombia](https://github.com/juanguzman2/Pronostico-de-la-evolucion-del-PIB-en-las-cuatro-economias-mas-grandes-de-Latinoamerica/blob/master/Imagenes/PibColombia.png?raw=true)

## Conclusiones

La evaluación de los modelos SARIMAX utilizados para predecir la serie de tiempo del PIB en dólares de Brasil, México, Argentina y Colombia proporciona información importante para la toma de decisiones económicas y para la evaluación del desempeño de los modelos de series de tiempo.

En el caso de Brasil, se observa una gran discrepancia entre los valores reales y los predichos, con un valor de RMSE de 728673516157 y un valor de MSE de 5.309650931486935e+23. Esto indica que el modelo SARIMAX utilizado no es adecuado y que se deben considerar otros modelos o enfoques para mejorar la precisión de las predicciones. Es importante evaluar la calidad de los datos utilizados para la construcción del modelo y ajustar los parámetros del modelo SARIMAX para obtener una mejor precisión en las predicciones.

En los casos de México, Argentina y Colombia, se observa una discrepancia moderada entre los valores reales y los predichos, con valores de RMSE de 141157525945, 77689486957 y 81459293289, respectivamente, y valores de MSE de 1.992544713098597e+22, 6.035656383672727e+21 y 6.635616463199854e+21, respectivamente. Esto indica que los modelos SARIMAX utilizados son adecuados y están haciendo predicciones precisas en cierta medida, pero aún hay un margen de mejora para mejorar la precisión de las predicciones.

Es importante seguir evaluando y mejorando los modelos utilizados para predecir la serie de tiempo del PIB en dólares de estos países, con el fin de tener predicciones más precisas y útiles para la toma de decisiones económicas. Además, se debe considerar el uso de otros modelos o enfoques, como modelos de aprendizaje automático o modelos basados en redes neuronales, para mejorar la precisión de las predicciones.

También es importante tener en cuenta que la precisión de las predicciones puede verse afectada por factores externos como cambios en las políticas económicas, eventos geopolíticos o desastres naturales. Por lo tanto, es necesario actualizar y ajustar regularmente los modelos utilizados para garantizar que las predicciones sean lo más precisas y útiles posible.

En conclusión, la evaluación de los modelos SARIMAX utilizados para predecir la serie de tiempo del PIB en dólares de Brasil, México, Argentina y Colombia proporciona información importante para la toma de decisiones económicas y para la mejora continua de los modelos utilizados. Los resultados sugieren que los modelos son adecuados y están haciendo predicciones precisas en cierta medida, pero aún hay un margen de mejora

## Conclusiones generales

Después de analizar la información, podemos concluir que la situación económica de Brasil es sólida y seguirá consolidándose como la economía más grande y sólida de Latinoamérica. A pesar de la desaceleración prevista para 2023, esto es una característica normal de los ciclos económicos y no debería ser motivo de preocupación.

En cuanto a México, podemos ver que la economía se proyecta con un crecimiento constante y potenciado, lo que sugiere un futuro económico sólido y prometedor. Las políticas del actual presidente, Manuel López Obrador, parecen estar contribuyendo a este crecimiento.

Sin embargo, en el caso de Argentina, la situación es más complicada. La mala gestión de las políticas públicas ha desembocado en grandes inflaciones, lo que se refleja en la gráfica y se proyecta un crecimiento más moderado y lento en el futuro. Es importante que el gobierno argentino tome medidas para solucionar este problema si desea mejorar su economía.

Finalmente, en cuanto a Colombia, vemos que la economía se proyecta con un crecimiento leve pero constante. Aunque las políticas del presidente Gustavo Petro no han contribuido mucho a impulsar la economía, la situación económica sigue siendo estable.

En general, podemos concluir que estas cuatro economías latinoamericanas están en proceso de recuperación después del impacto de la pandemia del COVID-19, lo que sugiere que habrá mejores oportunidades económicas y una mejora en la calidad de vida para los habitantes de la región. Además, se espera que el atractivo de las economías de Latinoamérica a nivel mundial aumente, lo que debería atraer más inversiones y oportunidades de crecimiento en el futuro.

## Consideracion

Si bien los modelos econometricos usados son muy utilizados, se pueden explorar otros modelos de Machine Learning que puedan tener una mejor prediccion

## Autor

Juan Esteban Guzman Saldarriaga

### Contacto

linkedin : www.linkedin.com/in/juan-guzmans

Celular: 3023060210

Correo : sojuanesi4@gmail.com
