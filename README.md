Classification de la rétinopathie diabétique par apprentissage profond
Ce dépôt contient le code et la méthodologie utilisés dans le cadre du projet : "Classification of Diabetic Retinopathy by Using a Deep Learning Model", réalisé dans le cadre du module PROJ419 à l’Université Libre de Bruxelles (ULB).

 Présentation du projet
La rétinopathie diabétique (RD) est une cause majeure de perte de vision dans le monde. Ce projet a pour objectif de développer un système automatisé capable de classifier des images du fond d’œil selon différents niveaux de sévérité de la RD à l’aide de techniques d’apprentissage profond.

Nous utilisons le jeu de données Kaggle "Diabetic Retinopathy - Resized" (dérivé de la compétition EyePACS 2015), et nous explorons un modèle hybride combinant :

L’apprentissage par transfert avec ResNet50

Une classification supervisée avec XGBoost

Le flux de travail inclut le prétraitement des images, l'équilibrage des classes, l'extraction de caractéristiques et l'évaluation des performances.

 Jeu de données
Source : Kaggle Diabetic Retinopathy (Resized)

Nombre total d’images utilisées : 3540 (708 images par classe après équilibrage)

 Méthodologie
Sous-échantillonnage pour corriger le déséquilibre des classes

Découpage en ensembles d'entraînement, validation et test

Augmentation des données via des générateurs d’images

Extraction des caractéristiques :

Caractéristiques profondes via ResNet50

Caractéristiques classiques (ex. couleur, texture)

Modélisation hybride :

Utilisation des caractéristiques extraites avec XGBoost

Ajustement fin de ResNet50 pour la classification

Évaluation des modèles : précision, matrice de confusion, etc.

 Dépendances
Installez les bibliothèques Python nécessaires avec :


pip install numpy pandas matplotlib scikit-learn xgboost tensorflow keras
Utilisation
Clonez le dépôt et exécutez le script principal :

git clone https://github.com/Niqaise/Proj-H419/blob/main/Projet%20419%20Classification.ipynb
cd diabetic-retinopathy-classification
python main.py
Assurez-vous que le jeu de données est placé dans le bon dossier ou modifiez le chemin dans le script.

 Résultats
Accuracy du modèle ResNet50 ajusté : [85%]

Accuracy du modèle XGBoost sur les caractéristiques extraites : [56%]

 Rapport
Pour une explication complète du projet, veuillez consulter le rapport PDF : ULBreport_Template.pdf

 Auteur
Milong Irene Niqaise
Université Libre de Bruxelles (ULB)
Email : irene.milong@ulb.be

Encadré par Prof. Olivier Debeir
