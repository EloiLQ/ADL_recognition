# Étude sur la Reconnaissance d'Activités Humaines à partir de Données d'Accélérométrie

Le suivi des activités quotidiennes d'un individu est rendu possible grâce aux mesures d'accélérométrie alliées aux méthodes d'intelligence artificielle. Pour réaliser une analyse des activités humaines, on dispose du jeu de données publique [Dataset for ADL Recognition with Wrist-worn Accelerometer Data Set](https://archive.ics.uci.edu/ml/datasets/Dataset+for+ADL+Recognition+with+Wrist-worn+Accelerometer). 
Les données d'accélérométrie sont mesurées avec un bracelet électronique porté par plusieurs individus effectuant un total de 14 ADL. Le bracelet mesure l'accélération au niveau du poignet selon les trois axes spatiaux x, y et z avec une fréquence de 25 Hz.

L'analyse est composée de deux parties : 
- une analyse exploratoire ([Clustering_HDBSCAN.ipynb](https://nbviewer.org/github/EloiLQ/ADL_recognition/blob/main/Clustering_HDBSCAN.ipynb))
- une modélisation statistique des ADL ([Identification.ipynb](https://nbviewer.org/github/EloiLQ/ADL_recognition/blob/main/Identification.ipynb))

L'analyse exploratoire permet de dégager des patterns au sein des signaux d'accélérométrie, tandis que la modélisation statistique permet de prédire les ADL en fonction des signaux d'accélérométrie.
Dans ce notebook, on réalise un échantillonnage des signaux avec une fenêtre de 4 secondes sans chevauchement. Les échantillons bruts sont structurés et échantillonnés afin d'être interprétés par un réseau de neuronnes. Ils sont également featurizés pour réaliser l'analyse exploratoire à partir d'outils d'apprentissage machine non-supervisés.

Le notebook [Featurization.ipynb](https://nbviewer.org/github/EloiLQ/ADL_recognition/blob/main/Featurization.ipynb) réalise la visualisation des données brutes et le calcul des features utilisés pendant la phase exploratoire. Enfin le notebook [TestData.ipynb](https://nbviewer.org/github/EloiLQ/ADL_recognition/blob/main/TestData.ipynb) échantillonne le jeu de données test non labellisé pour effectuer de prédictions à l'aide du modèle de classification.
