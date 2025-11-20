# Machine Learning – Ateliers & Travaux Pratiques

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Pandas_logo.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" height="90" />
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/22/TensorFlow_logo.svg" height="90" />
</p>

Bienvenue dans ce dépôt GitHub qui regroupe mes **travaux pratiques** et **ateliers** réalisés dans le cadre de l'apprentissage du module **Machine Learning**.
Chaque atelier est un projet indépendant illustrant une thématique précise (régression, classification, évaluation de modèles, feature engineering, etc.).

---
## Objectifs du dépôt
- Centraliser l'ensemble de mes ateliers Machine Learning
- Fournir un point d'entrée simple pour cloner et exécuter les notebooks
- Montrer la progression : des bases supervisées vers des techniques plus avancées
- Constituer une base réutilisable pour futures expérimentations

---
## Structure des Ateliers

| Atelier | Dossier | Thème | Contenu principal |
|--------|---------|-------|-------------------|
| **Atelier 1 – Régression** | [`Atelier1_Regression/`](Atelier1_Regression/) | Régression linéaire simple, multiple, polynomiale | Exploration, métriques (MSE, RMSE, MAE), rapport LaTeX détaillé. |
| **Coming Soon...** | [`/#`](/#) |  |  |

> Chaque dossier aura (ou possède) son propre `README.md` détaillant l'objectif, la structure et les instructions d'exécution.

---
## Technologies communes
| Catégorie | Outils |
|-----------|-------|
| Langage | Python 3.10+ |
| Manipulation | NumPy, Pandas |
| Visualisation | Matplotlib, Seaborn |
| Modélisation | scikit-learn (base), TensorFlow/Keras (avancé) |
| Évaluation | métriques sklearn, courbes ROC, confusion matrix |
| Environnement | Jupyter Notebook / VS Code |

---
## Installation globale
```bash
git clone https://github.com/MedGm/Machine-Learning.git
cd Machine-Learning

# Environnement virtuel (recommandé)
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Dépendances de base
pip install numpy pandas matplotlib seaborn scikit-learn

# (Optionnel pour ateliers avancés)
pip install tensorflow
```

---
## Utilisation d'un atelier
```bash
cd Atelier1_Regression/notebooks
jupyter notebook  # Ouvrir et exécuter les cellules
```
Les chemins des jeux de données sont relatifs (`../dataset/...`).

---
## Aperçu rapide de l'Atelier 1
L'atelier Régression inclut :
- Visualisation (scatter, matrice de corrélation, distributions)
- Régression linéaire simple (Salaire ~ Expérience) : interprétation de la pente
- Régression multiple (Charges ~ age + bmi + smoker) : importance des features
- Régression polynomiale (PIB Chine) : comparaison linéaire vs polynôme degré 3
- Rapport LaTeX compilable (`Atelier1_Regression/report/main.tex`)

---
## Export des figures (exemple générique)
```python
plt.savefig("../figures/nom_de_la_figure.png", dpi=120, bbox_inches="tight")
```
Convention d'appellation conseillée : `dataset_plotType.png`.

---
## Roadmap (prévisionnelle)
- [ ] Ajouter Atelier Classification (Logistic Regression + k-NN)
- [ ] Ajout scripts `run.py` pour exécution batch
- [ ] Intégrer tests simples (vérification tailles / métriques minimales)
- [ ] Ajouter `requirements.txt` généré automatiquement
- [ ] Mettre en place CI (lint + exécution notebook sans erreur)

---
## Contribution
Suggestions, corrections et améliorations bienvenues : ouvrez une issue ou une Pull Request.

---
## Auteur
Réalisé par **EL GORRIM Mohamed**  
Cycle Ingénieur LSI – Université Abdelmalek Essaâdi

---
## Licence
Usage éducatif et personnel. Mentionner la source en cas de réutilisation publique.

Bon apprentissage et exploration du Machine Learning !

