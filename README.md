# Description du Projet : Analyse de Sentiment sur les Données Twitter en Temps Réel
Ce projet vise à collecter des tweets en temps réel à l'aide de ntscraper de la bibliothèque Nitter, prétraiter ces tweets pour l'analyse de sentiment à l'aide de NLTK, et stocker les résultats dans une base de données MongoDB. L'objectif est d'obtenir des insights sur l'opinion publique concernant n'importe quel sujet en analysant la polarité des tweets (négative, neutre, positive).

# Fonctionnalités Clés :

Collecte de Données : Utilisation de ntscraper pour collecter des tweets pertinents depuis Twitter via Nitter , en mode hashtag et avec un nombre spécifié.

Exportation vers CSV : Les données collectées sont transformées en un DataFrame pandas pour une manipulation ultérieure. Ce DataFrame est ensuite exporté vers un fichier CSV nommé "ChatGPT_data.csv", contenant les colonnes pertinentes telles que le lien du tweet, le texte, la date, les likes et les commentaires.

Prétraitement des Tweets : Chaque tweet est prétraité pour normaliser le texte en remplaçant les mentions d'utilisateurs par "@user" et en réduisant la longueur maximale du tweet à 128 caractères.

Analyse de Sentiment : Utilisation d'un modèle de traitement du langage naturel pour analyser le sentiment de chaque tweet. Le modèle attribue des scores de négativité, neutralité et positivité à chaque tweet.

Stockage dans MongoDB : Les résultats de l'analyse de sentiment sont convertis en une liste de dictionnaires représentant chaque tweet avec ses scores associés. Ces données sont ensuite stockées dans une collection nommée "Nlp" dans une base de données MongoDB locale.

# Technologies Utilisées :

Python pour le développement et l'automatisation du processus
Pandas pour la manipulation des données et l'exportation vers CSV
MongoDB pour le stockage des résultats d'analyse de sentiment
Modèle de NLP pour l'analyse de sentiment, probablement basé sur des outils comme NLTK et des modèles pré-entraînés de traitement du langage naturel.

# Objectifs du Projet :

Ce projet permet de surveiller et d'analyser en temps réel l'évolution des opinions sur le sujet de l'intelligence artificielle (AI) à partir des tweets collectés. Les résultats stockés peuvent être utilisés pour générer des insights sur les tendances et les sentiments du public concernant l'IA sur Twitter.
