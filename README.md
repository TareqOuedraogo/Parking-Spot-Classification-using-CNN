# Parking-Spot-Classification-using-CNN
CNN-based image classification of parking spot availability (baseline, augmentation, transfer learning)

Projet  – Classification des Places de Stationnement
Présentation du projet
Ce projet consiste à développer et comparer différents modèles de Réseaux de Neurones Convolutifs (CNN) pour la classification de l'état des places de stationnement à partir d'images. Trois approches sont explorées : un CNN classique construit de zéro, un CNN avec augmentation de données, et un modèle basé sur l'apprentissage par transfert.

Contexte
La gestion intelligente des places de stationnement est un enjeu important pour les villes et les infrastructures privées. Ce projet aborde le problème de la classification automatique de l'état des places de stationnement à partir d'images, avec trois catégories distinctes.

Classes de classification
Classe 0 : Occupée - Place occupée par un véhicule
Classe 1 : Libre - Place vide et disponible
Classe 2 : Libre mais non disponible - Place vide mais réservée ou interdite
Méthodologie
1. Chargement et prétraitement des données
Chargement des images avec PyTorch DataLoader
Redimensionnement à une taille uniforme (ex: 224x224)
Normalisation des valeurs de pixel
Séparation en ensembles d'entraînement, validation et test
Justification de chaque étape de prétraitement
2. Modèle CNN classique (Baseline)
Architecture CNN construite de zéro avec PyTorch
Couches convolutives, pooling et fully connected
Fonctions d'activation ReLU
Dropout pour la régularisation
Entraînement avec CrossEntropyLoss et optimiseur Adam
Évaluation avec exactitude et matrice de confusion
Analyse des classes difficiles à distinguer
3. Modèle CNN avec augmentation de données
Implémentation de deux techniques d'augmentation minimum :
Rotation, translation, zoom aléatoires
Changements de luminosité/contraste
Flipping horizontal/vertical
Ajout de bruit
Comparaison des performances avec et sans augmentation
Analyse de l'impact sur la généralisation
4. Modèle CNN par apprentissage par transfert
Chargement d'un modèle pré-entraîné (ex: ResNet, VGG, EfficientNet)
Justification du choix du modèle
Deux approches d'adaptation :
Extraction de caractéristiques (feature extraction)
Ajustement fin (fine-tuning)
Comparaison des deux approches
Évaluation avec exactitude et matrice de confusion
Utilisation
