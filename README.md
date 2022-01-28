# SAE-15-TRAITER-DES-DONNEES
SAE 15 Consommation énergétique d'un dispositif LoRa

# Projet consommation électrique d'un dispositif de transmission LoRa

## Synopsis
Le projet temps de transmission Lora consiste à analyser les données relatives à la consommation énergétique d'un dispositif LoRa lors d'une transmission. 

## Données
Les données obtenues à partir d'un appareil de type Otii Arc et d'un Fipy Pycomm et ont été sauvegardées dans le dossier *data/raw*. La technologie LoRa permet à un utilisateur de choisir le facteur d'étalement, la bande passante ainsi que le taux de redondance des bits de données lors de la transmission. Le choix des paramètres de transmission influe sur le temps d'une transmission LoRa et donc la consommation du dispositif. Les données de l'expérience regroupent plusieurs transmissions avec différents paramètres listés ci-dessous. 

- Spreading factor (facteur d'étalement) : 7 ou 12,
- Bande passante : 125 kHz,
- Taux de bits redondants : 4/5, 4/6, 4/7, 4/8,
- Taille des données : 0-222 facteur d'étalement à 7), 0-51 (facteur d'étalement à 12).

Afin de mieux comprendre les données générées, le dossier references contient le code source embarqué par le Pycomm ainsi que le fichier de données original qui peut être ouvert en installant le logiciel Otii disponible à l'adresse suivante : https://www.qoitech.com/download/.

## Tâches
Les tâches demandées dans ce projet sont les suivantes.

1. Écrire un programme qui fusionne les fichiers csv (*dossier src/data*) pour ne former qu'un seul jeux de données.
2. Établir pour chaque variable le nombre de valeurs manquantes et aberrante ainsi que le pourcentage que cela représente.
3. Établir le nombre et le pourcentage d'observations qui ont des valeurs aberrantes et/ou manquantes.
4. Calculer la différence d'énergie consommée entre chaque observation.
5. Définir les fonctions ComputeMean et ComputeMedian et calculer (*src/model/model.py*) le courant médian lors de transmissions.
6. Afficher la courbe qui montre l'énergie total consommée en fonction du facteur d'étalement et du taux de redondance des bits. 
