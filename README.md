# ML-Project

Ce projet vise à prédire l’évolution du prix de l’action Apple (AAPL) à l’aide de techniques de Machine Learning et d’indicateurs techniques boursiers. L’objectif est de fournir des prédictions robustes pour aider à la prise de décision d’investissement, avec une interface chatbot pour interagir avec les résultats.

## Étapes du projet

### 1. Collecte et préparation des données

- **Source** : API Alpha Vantage (données historiques quotidiennes d’AAPL, OHLCV).
- **Chargement** : Utilisation de la librairie `alpha_vantage` pour récupérer les données.
- **Nettoyage** :
  - Conversion des dates.
  - Renommage des colonnes pour plus de clarté (`Open`, `High`, `Low`, `Close`, `Volume`).
  - Création de la variable cible `Target` (1 si le prix du lendemain est supérieur à celui du jour, 0 sinon).
  - Gestion des valeurs manquantes.

### 2. Feature Engineering

Ajout d’indicateurs techniques :
- Moyennes mobiles (SMA5, SMA20)
- RSI (Relative Strength Index)
- MACD et signal MACD
- Bandes de Bollinger (moyenne, supérieure, inférieure)
- Volatilité (écart-type mobile)
- Momentum
- Variation du jour précédent
- Volume relatif

### 3. Modélisation

- **Modèles testés** :
  - Random Forest Classifier (avec tuning du nombre d’arbres, gestion du déséquilibre avec SMOTE)
  - XGBoost Classifier (tuning des hyperparamètres)
- **Validation** :
  - Découpage temporel (TimeSeriesSplit)
  - Backtesting avec fenêtre glissante (sliding window)
  - Optimisation du seuil de classification (F1-score)
- **Évaluation** :
  - Accuracy, Precision, Recall, F1-score
  - Matrices de confusion et visualisations
  - Importance des features

### 4. Chatbot d’interprétation

- Interface interactive en Python pour :
  - Afficher les alertes de trading (hausses/baisses prévues avec confiance)
  - Résumer la tendance récente
  - Donner la prédiction pour la prochaine séance
  - Évaluer la performance du modèle (précision, retour sur investissement, comparaison buy & hold)
- Commandes disponibles : `alerte`, `résumé`, `demain`, `performance`, `sortir`


https://drive.google.com/drive/folders/1NsXzWhO6XNFc70yPITsUFLTF4pLuFH6_?dmr=1&ec=wgc-drive-globalnav-goto
