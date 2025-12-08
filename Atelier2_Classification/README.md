# Atelier 2 : Classification – Machine Learning

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Pandas_logo.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" height="90" />
</p>

## Structure du dossier
| Fichier / Dossier | Description |
|-------------------|-------------|
| `dataset/diabetes.csv` | Jeu de données Pima Indians Diabetes (binaire). |
| `notebooks/classification.ipynb` | Notebook principal : exploration, sélection de features, modèles. |
| `models/` | Emplacement des modèles sauvegardés (`joblib`). |
| `figures/` | Export des figures (nuages de points, matrices de confusion, courbes ROC). |
| `README.md` | Ce fichier. |

## Aperçu des Parties
### 1. Data Visualisation, Feature Selection & Normalisation
- Inspection des colonnes, types, valeurs aberrantes/à imputer.
- Statistiques descriptives (`describe()`, proportion cible).
- Visualisations : scatter matrix, distributions, corrélation.
- Sélection de variables : Univariate Selection, PCA, Recursive Feature Elimination, Feature Importance (forêt aléatoire).
- Normalisation / standardisation des attributs continus.

### 2. Classification & Évaluation
- Algorithmes : KNN, Decision Tree, MLP (ANN), Gaussian Naive Bayes, SVM (linéaire, polynomial, RBF).
- Sauvegarde / rechargement des modèles (`joblib`).
- Métriques : Accuracy, Log Loss, AUC ROC, Matrice de confusion, Classification report.
- Spot-checking : comparaison rapide multi-modèles (validation croisée).
- Ensemble learning : Bagging, Stacking, Boosting (GradientBoosting/AdaBoost).
- Prédictions sur un jeu de test dédié.

## Jeu de données
- Source recommandée : Kaggle – [Pima Indians Diabetes Database](https://www.kaggle.com/kumargh/pimaindiansdiabetescsv)  
- Format attendu : fichier CSV nommé `diabetes.csv` placé dans `dataset/`.  
  Colonnes typiques : `Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, Age, Outcome`.
- Si le fichier n'est pas présent, le notebook propose un téléchargement de secours via une source publique (raw GitHub).

## Technologies
- Python 3.10+
- NumPy / Pandas / Matplotlib / Seaborn
- scikit-learn
- Jupyter Notebook
- joblib (inclus avec scikit-learn)

### Installation rapide
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Exécution du notebook
```bash
cd Atelier2_Classification/notebooks
jupyter notebook
```
Les chemins des jeux de données et modèles sont relatifs (`../dataset/`, `../models/`).

## Export des figures (exemple)
```python
plt.savefig("../figures/roc_knn.png", dpi=120, bbox_inches="tight")
```
Figures recommandées :
```
scatter_matrix_diabetes.png
correlation_heatmap_diabetes.png
confusion_matrix_*.png
roc_curve_*.png
spot_check_barplot.png
```

## Métriques indicatives (à recalculer)
| Modèle | Accuracy (cv) | Commentaire |
|--------|---------------|-------------|
| KNN | ~0.74 | Sensible au scaling et au choix de k |
| Decision Tree | ~0.72 | Interprétable, risque d'overfit |
| MLP | ~0.78 | Peut gagner avec tuning (hidden layers, l2) |
| GaussianNB | ~0.74 | Baseline rapide |
| SVM linéaire | ~0.78 | Bon sur données scalées |
| SVM poly / RBF | ~0.79 | Ajuster `C` et `gamma` |
| Bagging / Boosting | ~0.80+ | Souvent meilleure robustesse |

## Idées d'extensions
- Gérer le déséquilibre (threshold tuning, class weights, SMOTE).
- Courbes d'apprentissage et validation.
- Optimisation d'hyperparamètres (GridSearchCV / RandomizedSearchCV).
- Calibration des probabilités (CalibratedClassifierCV).

## Auteur
Réalisé par **EL GORRIM Mohamed** – Cycle Ingénieur LSI


