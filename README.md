[:es: Ir a versión en Español](https://github.com/iseka-dev/DataScience-Projects/new/master/BAIRES_project/README.sp.md)

### BAIRES Project   :chart_with_upwards_trend:
#### Analysis and prediction of the real state market in Buenos Aires
[Go to notebook](https://github.com/iseka-dev/DataScience-Projects/tree/master/BAIRES_project/HousePricing_BsAs.ipynb)

### :information_source: Description 

The project can be considered at three stages.

1. First, **preprocessing**. The dataset is cleaned and prepared (Droping columns and rows with missing or null values, calulating and imputing data wisely to not generate a bias in the model then).
2. Then, **price and location** of properties in Ciudad Autonoma de Buenos Aires (CABA) is **analysed**. Cheapest and most expensive neighborhood are identified. Also, it is shown that real locations and published locations mismatch a lot of times, and most of times *published location correspond with more expensive areas*.
3. At stage 3 remaining preprocessing is done and **binaries** are created. Then two models are trained: **DecisionTreeRegressor** and **KNeighbours**. A test set was curated for final evaluation, while train set was partitioned in several manners for evaluation: with simple *train_test_split*, and with *Kfold* implementation. *GridSearch* was used for **optimization**. And **root mean square error** (RMSE) was adopted as error measure.

Finally, the **models can predict price of properties** with an estimated error of +/-$ 40000 (depending de model)

Skills: Python, Scikit-learn, Matplotlib, Seaborn, Crossvalidation, DecisionTreeRegressor, KNeighbours, Pandas, Numpy

*Datos provided by <a href='https://www.properati.com.ar/data'>Properati</a>*

### :telescope: Dataset attributes

* id: property id
* created_on: when property was uploaded to the website
* operation: rent or sell)
* property_type: house, department, store, PH
* place_with_parent_names: Where is located the property, according to the publisher
* lat-lon: coordinates
* lat: latitude
* lon: longitude
* price_aprox_usd: aproximated price in usd
* surface_total_in_m2: Total surface (in square meters)
* surface_covered_in_m2: Covered surface (in square meters)
* price_usd_per_m2: price per square meter in usd (price / surface)
* floor: floor number (if appropriate)
* rooms: number of rooms
* expenses: exenses (if appropriate)
* barrio: neighborhood in agrreement with official charts.
* properati_url: url of publication in Properati
