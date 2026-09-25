# Analyse des données énergétiques européennes

## Présentation

Ce projet a été réalisé dans le cadre du Master Ingénierie Mathématique et Data Science.

L'objectif est d'analyser les données énergétiques de plusieurs pays européens à partir du jeu de données Our World in Data.

Le projet combine l'utilisation de Python, MongoDB et des outils de visualisation afin d'étudier les différences entre plusieurs pays européens et l'évolution de leur consommation énergétique.

## Données

Source : Our World in Data \- Energy

Le jeu de données contient des informations sur :

- la consommation énergétique ;  
- la production d'électricité ;  
- les différentes sources d'énergie ;  
- la population ;  
- le PIB ;  
- les émissions et d'autres indicateurs énergétiques.

Les données sont organisées par pays et par année.

## Objectifs du projet

- Sélectionner les pays européens présents dans le dataset.  
- Stocker les données dans MongoDB Atlas avec un document par pays.  
- Comparer le mix électrique de la France et de l'Allemagne.  
- Comparer leur mix énergétique global.  
- Étudier l'évolution de la consommation énergétique en France.  
- Analyser les corrélations entre consommation énergétique, population et PIB.  
- Créer des visualisations interactives avec Plotly et Dash.

## Technologies utilisées

- Python  
- Pandas  
- NumPy  
- MongoDB Atlas  
- PyMongo  
- Matplotlib  
- Plotly  
- Dash  
- Google Colab

## Organisation des données

Les données ont d'abord été chargées à partir d'un fichier JSON, puis filtrées afin de conserver les pays européens utilisés dans l'analyse.

Les données ont ensuite été stockées dans MongoDB Atlas avec un document par pays.

Chaque document contient :

- le nom du pays ;  
- son code ISO ;  
- les données énergétiques annuelles.

Exemple de structure :

{ "country": "France", "iso\_code": "FRA", "data": \[ { "year": 2023 } \] }

## Analyses réalisées

### Comparaison du mix électrique France \- Allemagne

Une première analyse compare la part des principales sources dans la production d'électricité des deux pays.

La France reste fortement marquée par le nucléaire, même si sa part a diminué au cours des dernières années.

En Allemagne, le mix électrique est plus diversifié. La part du charbon et du nucléaire a diminué, tandis que l'éolien et le solaire ont fortement progressé.

### Comparaison du mix énergétique global

Une seconde comparaison porte sur le mix énergétique global, c'est-à-dire la part des différentes sources dans la consommation énergétique totale.

En 2023, la France se distingue par une forte présence du nucléaire et du pétrole.

En Allemagne, le pétrole, le gaz et le charbon occupent une place plus importante, tandis que le nucléaire est devenu très faible.

Cette analyse permet de distinguer clairement le mix électrique du mix énergétique global.

### Évolution de la consommation énergétique en France

L'étude de la consommation énergétique française montre des évolutions différentes selon les sources.

Le nucléaire et le pétrole restent parmi les principales sources d'énergie.

La consommation de charbon diminue fortement au fil du temps.

À l'inverse, le solaire et l'éolien progressent progressivement, en particulier à partir des années 2010\.

## Analyse des corrélations

L'analyse des corrélations a été réalisée sur la période 1965-2022.

La consommation énergétique totale utilisée correspond à la variable `primary_energy_consumption` du dataset.

Les résultats montrent :

- une très forte corrélation positive entre la population et le PIB : environ 0,99 ;  
- une corrélation positive entre la population et la consommation énergétique totale : environ 0,77;  
- une corrélation positive entre le PIB et la consommation énergétique totale : environ 0,79.

Cependant, les nuages de points montrent que ces relations ne sont pas parfaitement linéaires.

Pour certaines périodes, la consommation énergétique peut diminuer alors que la population ou le PIB continuent d'augmenter.

D'autres facteurs peuvent donc influencer la consommation énergétique, comme l'efficacité énergétique, les évolutions technologiques ou les changements dans le mix énergétique.

Une corrélation ne permet pas d'établir directement une relation de causalité.

## Visualisations

Plusieurs visualisations ont été réalisées avec Matplotlib et Plotly :

- évolution du mix électrique français ;  
- évolution du mix électrique allemand ;  
- comparaison France \- Allemagne en 2023 ;  
- comparaison du mix énergétique global ;  
- évolution de la consommation énergétique française ;  
- matrice de corrélation ;  
- nuages de points entre consommation, population et PIB.

## Dashboard interactif

Un dashboard interactif a également été réalisé avec Plotly et Dash.

Il permet de sélectionner :

- un pays : France ou Allemagne ;  
- une source d'électricité.

Le graphique est ensuite mis à jour automatiquement afin de visualiser l'évolution de la part de cette source dans la production d'électricité.

## Principaux résultats

L'analyse met en évidence plusieurs différences entre la France et l'Allemagne.

La France présente une forte dépendance au nucléaire, notamment dans sa production électrique.

L'Allemagne présente un mix plus diversifié, avec une place importante du charbon, du gaz, de l'éolien et du solaire.

L'étude de la France montre également une diminution du charbon et une progression des énergies renouvelables comme le solaire et l'éolien.

Enfin, les analyses de corrélation montrent que la consommation énergétique totale est globalement liée à l'évolution de la population et du PIB, tout en restant influencée par d'autres facteurs.

## Organisation du projet

M1\_IMDS\_Energy/

- energy\_europe\_analysis.ipynb  
- owid-energy-data.json  
- README.md  
- images/  
- outputs/

## Compétences mises en pratique

Ce projet a permis de mettre en pratique plusieurs compétences :

- manipulation de données JSON ;  
- analyse et transformation de données avec Pandas ;  
- stockage et interrogation de données avec MongoDB ;  
- connexion à MongoDB Atlas avec PyMongo ;  
- visualisation de données avec Matplotlib ;  
- visualisations interactives avec Plotly ;  
- création d'un dashboard avec Dash ;  
- analyse exploratoire de données ;  
- analyse de corrélations.

## Auteur

Naima Assoulaimani

Master Ingénierie Mathématique et Data Science  
Université de Haute-Alsace