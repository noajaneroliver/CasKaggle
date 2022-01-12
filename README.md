# Pràctica Kaggle APC UAB 2021-22
### Nom: Noa Janer Oliver
### DATASET: World happiness report
### URL: https://www.kaggle.com/unsdsn/world-happiness

## Resum
Aquest dataset és el resultat de l'enquesta mundial de Gallup enquesta realitzada a 155 països sobre la felictat. L'enquesta demana als enquestats que pensin en una escala amb la millor vida possible per a ells amb un 10 i la pitjor vida possible amb un 0 i que valorin les seves pròpies vides actuals en aquesta escala. Les columnes que segueixen la puntuació de la felicitat estimen fins a quin punt cadascun dels sis factors que explicaré més endavant contribueixen a fer que les avaluacions de la vida siguin més elevades a cada país que a la Distòpioa (païs hipotètic que té valors iguals a les mitjanes nacionals més baixes del món per a cadascún dels dis factors). No tenen cap impacte en la puntuació total de cada país, però sí que expliquen per què alguns països es classifiquen més alt que d'altres.

En aquest dataset tenim les dades obtingudes des de l'any 2015 fins al 2019. El que he fet per fer predicció de la felicitat es ajuntar els 5 datasets i tractar cada mostra dels països en diferents anys com diferents països, és a dir que en total tenim unes 600 mostres. I enlloc de tenir en compte el païs tindrem en compte la regió a en la que s'ha realitzat l'enquesta que he afegit com a noves columnes categóriques. 

Finalment les columnes que tenim per analitzar són: 

|NAME|TYPE|
|--|--|
|Economy (GDP per capita)|float|
|Family Tree|float|
|Health (Life Expectancy)|float|
|Freedom|float|
|Trust (Government Corruption)|float|
|Generosity|float|
|Region_Australia and New Zealand|float|
|Region_Central and Eastern Europe|float|
|Region_Eastern Asia|float|
|Region_Latin America and Caribbean|float|
|Region_Middle East and Northern Africa|float|
|Region_North America|float|
|Region_Southeastern Asia|float|
|Region_Southern Asia|float|
|Region_Sub-Saharan Africa|float|
|Region_Western Europe|float|


Com podem veure la columna que fa referéncia a la felicitat al país ja no hi és perque està separada i adjudicada com a 'target' per a la predicció. Com la columna 'Happiness Rank' prenia valors de 1 fins a 155, això és auna cardinalitat massa gran, així que he convertit l'atribut en un de categóric dividint els països entre si es trobaven al 'top 20' (1) del rang de felicitat o no (0).

També he tractat els valors nuls, les columnes que tenien el 80% de valors nuls han estat eliminades, altres com la regió les he tractat afegint la regió més comuna del païs al que pertanyen. 

###Models

Observem que la nostra classe objectiu consta de moltes més mostres de tipus 0 que no 1, és a dir no està balencejada. És per això que els dos models que ajustaré els avaluaré segons l'f1 score. 

He començat per ajustar un DecissionTreeClassifier a les dades buscant els millors hyperparàmetres amb GridSearchCV i RandomizedSearchCV. he observat que els valors que obtenia variaven una mica segons l'execució, així que he realitzat la cerca 10 cops amb cada tipus de cerca i finalment m'he quedat amb els valors més repetits.
He fet el mateix amb el model de Logistic regression i els hyperparametres amb els que m'he quedat son:

|MODEL|HYPERPARÀMETRES|ACCURACY|
|Logistic Regression|Default|0.8710|
|Decision Tree|max_depth=11, criterion='entropy', max_features = 6, splitter = 'random'|0.9090|






