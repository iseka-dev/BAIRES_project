[:uk: English version](https://github.com/iseka-dev/baires-project/blob/master/README.md)

### Proyecto BAIRES  :chart_with_upwards_trend:
#### Análisis y predicción del mercado inmobiliario en Ciudad Autónoma de Buenos Aires
[Click aquí para ir al notebook](https://github.com/iseka-dev/baires-project/blob/master/HousePricing_BsAs.ipynb)

### :information_source: Descripción del proyecto 

El proyecto puede ser considerado en tres etapas:

1. Primero, el **preprocesamiento**. El data set es limpiado, dejando de lado las columnas y observaciones con valores faltantes o null. Cuando fuere posible se imputan los datos ausentes.
2. Luego se *analiza* el **precio** y la **locación** de las propiedades en la Ciudad Autónoma de Buenos Aires (CABA). Los barrios más caros y más baratos son identificados. También se muestra que la ubicación real y la publicada no siempre coinciden, y puede observarse una tendencia a publicar ubicaciones de barrios vecinos *mas caros*.
3. En la etapa 3 se lleva se configuran las categorías en términos binarios. Luego se entrenan dos modelos: **DecisionTreeRegressor** and **KNeighbours**. Se reserva un set de testeo para la evaluación final, y el set de entrenamiento inicial se particiona con *train_test_split*, y con *Kfold* para diversas pruegas. *GridSearch* es usado para **optimización**. Como medida de error se adopta la **raiz del error cuadrático medio** (RMSE).

Finalmente, el modelo puede **predecir el precio de propiedades** con un error estimado de +/-$ 40000 (dependiendo el modelo).

Skills: Python, Scikit-learn, Matplotlib, Seaborn, Crossvalidation, DecisionTreeRegressor, KNeighbours, Pandas, Numpy

*Datos provistos por [Properati](https://www.properati.com.ar/data)

### :telescope: Atributos del dataset: 

* id: id de la propiedad
* created_on: fecha en la que la propiedad ingresó al sitio
* operation: alquiler (rent) o venta (sell)
* property_type: tipo de propiedad (casa, departamento, ph, etcétera)
* place_with_parent_names: nombre del lugar donde se encuentra la propiedad según el publicador
* lat-lon: coordenadas concatenadas
* lat: latitud
* lon: longitud
* price: precio en la moneda especificada en currency
* currency: divisa en la que está expresada la publicación
* price_aprox_usd: precio aproximado en dólares estadounidenses
* surface_total_in_m2: superficie total (en metros cuadrados)
* surface_covered_in_m2: superficie cubierta (en metros cuadrados)
* price_usd_per_m2: precio por metro cuadrado en dólares (precio dólares / superficie)
* floor: número de piso (si corresponde)
* rooms: cantidad de ambientes
* expenses: expensas (si corresponde)
* barrio: barrio según cartografía oficial
* properati_url: url de la publicación en Properati

 :arrow_right: Este proyecto fue desarrollado en el marco del curso de DATA SCIENCE de ACAMICA.
