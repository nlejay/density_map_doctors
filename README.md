# Carte de densité de médecins généralistes en France métropolitaine

Ce projet contient le notebook medecins.ipynb dans lequel figure tout le code ayant permis de tracer la carte.

## Données
Pour effectuer ce travail de calcul et de représentation graphique, les fichiers suivants ont été utilisés :

- offre_sante.xlsx : fichier regroupant le nombre de médecins généralistes par commune (source : Observatoire des territoires / année 2020)
- georef-france-bassin-vie-2012.geojson : fichier regroupant les bassins de vie ainsi que les données géographiques correspondantes (source : INSEE / 2012)
- communes-frmetdrom.geojson : fichier des différentes communes françaises avec leur données géographiques (source : https://github.com/gregoiredavid/france-geojson)
- pop_communes.csv : fichier contenant la population de chaque commune au recensement de 2019 (source : INSEE). La population des communes se trouve aussi dans les données précédentes mais n'ayant pas la date d'actualisation des données, je préfère utiliser un jeu de données actualisé lors du dernier recensement.

Tous ces fichiers sont accessibles avec le notebook sauf le fichier volumineux communes-frmetdrom.geojson (téléchargeable directement en suivant le lien donné ci-dessus)

## Remarques
Au lieu de créer une carte de densité de médecins par commune, j'ai préféré utiliser le découpage géographique des bassins de vie. En effet, une petite commune peut ne pas posséder de médecin mais être située à côté d'une grande commune qui elle en possède. Les habitants de la petite commune ont donc un accès à des médecins généralistes. Le calcul de densité par commune ne me semble pas approprié.

Le bassin de vie est défini par l'INSEE selon ces termes : le bassin de vie constitue le plus petit territoire sur lequel les habitants ont accès aux équipements et services les plus courants. Ce découpage géographique est plus approprié pour ce projet.

Il s'agit d'un de mes premiers projets de data manipulation/data visualisation.Toute remarque concernant ce travail est la bienvenue.
