Projet Big Data – Analyse Comparative du Clustering K-means: Scikit-learn vs Apache Spark

Ce projet propose une étude approfondie et expérimentale de l’algorithme de clustering K-means, comparé dans deux environnements de calcul complémentaires :
Scikit-learn → calcul local en mémoire
Apache Spark (PySpark) → calcul distribué pour environnements Big Data

L’objectif est d’évaluer comment l’architecture de calcul influence : les performances temporelles, l’utilisation des ressources (CPU / RAM), la qualité du clustering, et la scalabilité sur des volumes de données croissants.

📘 Contenu du notebook

Le notebook fourni reproduit l’ensemble du workflow d’un projet Big Data :

🔧 Prétraitement des données (Normalisation, encodage catégoriel, correction via One-Hot Encoding (important pour le dataset Adult)

🌀 Implémentation du clustering K-means

Version Scikit-learn

Version PySpark

📊 Mesures et analyses expérimentales: Temps d’exécution, consommation CPU / RAM, inertie et silhouette Score

📈 Jeux de données testés:
Wine Quality (petit)
Adult Dataset (moyen)
Données synthétiques Scikit-learn : 50k, 100k, 200k
Données Spark : 100k et 300k en 10 dimensions

🎨 Visualisations
Graphiques comparatifs
Analyse des tendances
Interprétation des résultats

🎯 Objectifs pédagogiques et scientifiques
Comprendre le comportement réel de K-means en local vs distribué
Identifier les limites du calcul local face au volume et à la dimension
Analyser l’importance du prétraitement (normalisation, encodage correct)
Évaluer la scalabilité de K-means
Définir les contextes d’utilisation appropriés pour Scikit-learn et Spark

⚠️ Point méthodologique clé

Lors du traitement du dataset Adult, un premier encodage naïf des variables catégorielles (encodage par entiers) a généré :
des distances artificielles,
un clustering non interprétable.

La correction par One-Hot Encoding a rétabli :
la cohérence géométrique des données,
la validité mathématique du clustering,
l'interprétabilité des résultats.

🛠️ Technologies utilisées
Python 3
Scikit-learn
Apache Spark (PySpark)
Pandas / NumPy
Matplotlib

📁 Fichier fourni

TPbigdata(3).ipynb — Notebook complet contenant : Implémentations, mesures expérimentales, visualisations, analyses.

🎓 Contexte
Projet réalisé dans le cadre du module Data Science – Master Ingénierie des Systèmes Complexes - Transformation Numérique pour l'Industrie.
