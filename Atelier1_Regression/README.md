# Atelier 1 : Régression – Machine Learning

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Pandas_logo.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" height="90" />
</p>

## Structure du dossier
| Fichier / Dossier | Description |
|-------------------|-------------|
| `dataset/Salary_Data.csv` | Données Expérience / Salaire (2 colonnes). |
| `dataset/insurance.csv` | Données assurance (âge, sexe, IMC, enfants, fumeur, région, charges). |
| `dataset/china_gdp.csv` | PIB de la Chine (1960–2014). |
| `notebooks/regression.ipynb` | Notebook principal de l'atelier (4 parties). |
| `figures/` | Emplacement des figures exportées (à générer). |
| `README.md` | Ce fichier. |

## Aperçu des Parties
### 1. Data Visualisation
- Inspection des colonnes, types, valeurs manquantes, statistiques (`describe()`)
- Visualisations : nuage de points Salaire vs Années d'expérience, scatter matrix assurance, matrice de corrélation, distribution des charges.

### 2. Régression Linéaire Simple
- Modèle : `LinearRegression` (scikit-learn)
- Forme : `Salary = a * YearsExperience + b`
- Interprétation : ~9.4 k€ ajoutés par année d'expérience (approx.)
- Metrics (exemple) : MAE ≈ 6.3 k€, RMSE ≈ 7.1 k€

### 3. Régression Linéaire Multiple
- Features : `age`, `bmi`, `smoker`
- Prétraitement : standardisation + encodage fumeur (0/1)
- Metrics (exemple) : MAE ≈ 4.26 k$, RMSE ≈ 5.87 k$
- Tabagisme = facteur dominant

### 4. Régression Polynomiale (China GDP)
- Croissance non linéaire
- Comparaison modèle linéaire vs polynôme degré 3 (et test degré 10)
- Degré 3 = compromis précision / généralisation

## Technologies
- Python 3.10+
- NumPy / Pandas / Matplotlib / Seaborn
- scikit-learn
- Jupyter Notebook

### Installation rapide
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Exécution du notebook
```bash
cd Atelier1_Regression/notebooks
jupyter notebook
```

## Export des figures (exemple)
```python
plt.savefig("../figures/scatter_salary_experience.png", dpi=120, bbox_inches="tight")
```
Recommandés :
```
scatter_salary_experience.png
linear_regression_salary.png
scatter_matrix_assurance.png
insurance_corr_heatmap.png
charges_distribution.png
insurance_real_vs_pred.png
china_gdp_linear_vs_poly.png
```

## Métriques indicatives
| Modèle | MAE | RMSE | Commentaire |
|--------|-----|------|-------------|
| Linéaire simple (Salaire) | ~6.3 k€ | ~7.1 k€ | Tendance globale |
| Linéaire multiple (Assurance) | ~4.26 k$ | ~5.87 k$ | Tabagisme dominant |
| Linéaire (China GDP) | élevé | élevé | Non adapté |
| Polynôme degré 3 (GDP) | ↓ | ↓ | Bon compromis |

## Idées d'extensions
- Ajouter R²
- Tester Ridge / Lasso
- Interactions (`smoker * bmi`)
- Transformation log(charges)

## Auteur
Réalisé par **EL GORRIM Mohamed** – Cycle Ingénieur LSI
