# Projet

L'objectif principal de ce projet est de permettre aux étudiants de développer des compétences pratiques dans la gestion et l'analyse de données massives. En choisissant une source de données parmi celles proposées, les étudiants - en groupe de 3 ou 4 - devront mettre en oeuvre un pipeline complet, allant de la collecte à l’analyse et à la visualisation des résultats.

Choisissez parmi les sujets suivants :

## Sujets

- Mobilité : [API temps réel Naolib](https://data.nantesmetropole.fr/explore/dataset/244400404_api-temps-reel-tan/information/)
- Mobilité : [Plateform Régionale d'information pour la mobilité (Ile de France) ](https://prim.iledefrance-mobilites.fr/fr)
- Aviation : [OpenSkyNetwork API](https://openskynetwork.github.io/opensky-api/index.html)
- Réseaux sociaux : [Bluesky]([https://docs.bsky.app/docs/category/http-reference])
- Transports : [SNCF API Open-Data](https://numerique.sncf.com/startup/api/)
- Transports : [Here maps](https://developer.here.com/develop/rest-apis)

### Autres ?

Si vous souhaitez analyser une autre API, faites-moi une proposition par mail.

### Conseils

Attention aux limites d'utilisation (rate limit) : vérifiez bien celles de l'API que vous utilisez pour éviter d'être bloqués. N'hésitez pas à créer plusieurs comptes si nécessaire et évitez de consommer tous vos crédits trop vite.

## Consignes

Les groupes devront être compris entre 3 et 4 élèves. Pour ceux qui sont en difficulté avec les installations (problème de mémoire ou de puissance de leur machine), veillez bien à vous inclure dans un groupe n'ayant pas de soucis à ce niveau.

Vous devrez, à l'aide de Kafka et Apache Spark :

- effectuer deux requêtes différentes en mode batch avec état (dont une sans fenêtre),
- effectuer deux requêtes différentes en mode streaming avec fenêtre,
- effectuer une requête à l'aide de SparkSQL,
- réaliser une requête en mode batch et présenter les résultats sous forme de graphique à l'aide de Pandas et Seaborn.
- relier vos requêtes de Streaming à un dashboard
- (facultatif) intégrer des données provenant de deux sources à l'aide d'une jointure. Il peut s'agir du même topic -tel une auto-jointure en SQL- si cela fait sens.

Une première étape sera d'insérer dans Kafka les données. Vous pouvez vous prendre comme modèle le script [init-thingspeak-kafka.ipynb](init-thingspeak-kafka.ipynb), mais vous aurez des modifications à réaliser sur ce dernier.
Le dashboard pourra s'alimenter auprès de n'importe quelle source.

Les requêtes développées devront avoir du sens en regard des données : gardez à l'esprit que vous devrez préciser une synthèse des résultats obtenus et expliquer leur signification.

## Critères d'évaluation

Collecte des données (script d'initialisation dans Kafka) : 20 %
Mise en oeuvre technique (jobs Spark) : 40 %
Analyse et conclusions : 30 %
Présentation : 10 %

## Thématiques d'approfondissement

Choisissez sur Moodle un sujet parmi les 5 suivants :

- Elastic
- Formats de données (Avro, Parquet, ORC)
- SparkML
- GraphX
- Apache Flink

Vous aurez à faire l'intégration de cette thématique dans votre projet (cela peut être sur une sous partie), et à présenter à ce sujet.

## Présentation de la thématique d'approfondissement

Une présentation de 15 minutes (10 minutes de présentation de la thématique approfondie, et 5 minutes sur l'intégration dans le projet) sera à faire vendredi 21/02 après-midi devant la classe. Cette présentation sera suivie de 5 minutes de questions.

## Livrables attendus

Chaque groupe devra rendre pour le 21/02/2025, 23:59 un fichier ZIP comprenant :

- un bref rapport PDF comprenant les sections suivantes :
  - introduction décrivant l'API choisie et ses fonctionnalités
  - description des commandes de l'API utilisées et liste des attributs du flux
  - résultats obtenus et explications
  - conclusion
- les notebook Jupyter utilisés, comprenant en commentaire les besoins
- les sources et scripts permettant de reproduire le comportement (de préférence à l'aide de Docker Compose)

## Séance du 24/02/2024

Le but de cette séance sera de réaliser une discussion entre l'enseignant et chaque élève pour valider sa compréhension des concepts nécessaires aux projets rendus. Un échange de 5 minutes par étudiant aura lieu pour effectuer cette évaluation.
