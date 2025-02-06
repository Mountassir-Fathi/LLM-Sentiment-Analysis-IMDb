Comparaison de l'Analyse des Sentiments avec des LLMs Ajustés

Auteurs: FATHI MOUNTASSIR 
Institution : Université Hassan II-Casablanca, Faculté des Sciences Ben M'sick  

 📝 Introduction

Ce projet explore l'utilisation des Large Language Models (LLMs) pour l'analyse des sentiments à partir du dataset IMDb. Les modèles utilisés sont DistilBERT, DistilRoBERTa et GPT-2, ajustés (fine-tuning) pour classifier les critiques de films en sentiments positifs ou négatifs.

Les LLMs, bien que polyvalents, nécessitent souvent un ajustement spécifique pour des tâches particulières comme l'analyse de sentiments dans des domaines spécifiques.

🎯 Objectif

L'objectif de ce projet est de comparer les performances des modèles DistilBERT, DistilRoBERTa et GPT-2 sur la classification des sentiments à partir du dataset IMDb.

Nous évaluons leurs performances en termes de :
- Précision,
- Temps d'entraînement,
- Efficacité des ressources,

afin de déterminer le meilleur compromis pour des applications réelles.

📊 Méthodologie

1️⃣ Chargement et Prétraitement du Dataset
- Utilisation du dataset IMDb contenant des critiques de films étiquetées en positif/négatif.
- Prétraitement des données (nettoyage, suppression du bruit textuel, normalisation).

2️⃣ Tokenization et Préparation des Données
- Tokenisation des textes avec DistilBERT tokenizer pour transformer les données textuelles en entrées exploitables.
- Encodage des labels (0 pour négatif, 1 pour positif).

3️⃣ Fine-Tuning des Modèles
- Ajustement des modèles pré-entraînés (DistilBERT, DistilRoBERTa, GPT-2).
- Optimisation avec **AdamW** et ajustement des hyperparamètres (taux d'apprentissage, taille du batch).

4️⃣ Évaluation des Modèles
- Entraînement sur 80% du dataset, avec 20% réservés à la validation.
- Métriques utilisées : Accuracy, Training Los, Validation Loss.

🔍 Analyse des Résultats
- GPT-2 atteint la meilleure précision (94.07%), mais son entraînement est plus long et demande plus de ressources.
- DistilBERT offre une performance comparable (94.04%), avec une empreinte mémoire plus légère.
- DistilRoBERTa est le plus rapide à entraîner, mais affiche une précision légèrement inférieure (92%).

🛠️ Installation

Pour exécuter ce projet, suivez ces étapes :

```bash
# Cloner le dépôt Git
git clone https://github.com/Mountassir-Fathi/LLM-Sentiment-Analysis-IMDb.git
cd LLM-Sentiment-Analysis-IMDb
```