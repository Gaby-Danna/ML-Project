# ML-Project

C'est un projet de prédiction des valeurs boursières, le but est de prédire la valeur qu'aura une action par exemple. 
Pour ce faire, j'ai eu recours à l'utilisation des données boursière présentent sur l'API d'Alpha Vantage. 

## Données utilisées :

- Données historiques quotidiennes des actions telles que Apple
- Contenant les prix OHLC (Open, High, Low, Close) et le volume
- Période : Données complètes disponibles depuis l'introduction en bourse
  
## Source :

- API Alpha Vantage (https://www.alphavantage.co/support/#api-key)
- Clé API gratuite

### Méthodes Employées

Approche globale :
Préparation des données :
- Nettoyage des valeurs manquantes
- Feature engineering (moyennes mobiles, RSI, etc.)
- Normalisation MinMax

  Modélisation :
- Modèles classiques : ARIMA, Prophet, XGBoost
- Validation temporelle

### Objectifs

Prédire les valeurs futures des actions (Close) pour :
- Aide à la décision d'investissement
- Optimisation des portefeuilles
- Détection d'opportunités de trading

### Choix modèles de ML 

ARIMA : Simple et facilement interprétable 
- Choix initial pour établir une baseline
- Efficace sur séries stationnaires
- Paramètres (p,d,q) optimisés via auto_arima

Prophet : 
- Alternative simple pour comparaison
- Gère automatiquement : Saisonnalités hebdomadaires/annuelles + Jours fériés + Outliers

XGBoost : 
- Gère bien les relations non linéaires 
- Optimisation facile
- Résiste bien aux outliers 


https://drive.google.com/drive/folders/1NsXzWhO6XNFc70yPITsUFLTF4pLuFH6_?dmr=1&ec=wgc-drive-globalnav-goto
