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
|Trust (Government Corruption)|Default|
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
