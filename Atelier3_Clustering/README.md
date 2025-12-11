# Atelier 3 : Clustering

## Objectif
Pratiquer les concepts du clustering en traitant les données du Credit Card Dataset.

## Dataset
- **Credit Card Dataset** : [Kaggle Link](https://www.kaggle.com/arjunbhasin2013/ccdata)
- Télécharger le fichier `CC GENERAL.csv` et le placer dans le dossier `dataset/`

## Structure du projet
```
Atelier3_Clustering/
├── dataset/
│   └── CC GENERAL.csv
├── figures/
├── models/
├── notebooks/
│   └── clustering.ipynb
└── README.md
```

## Contenu de l'atelier

### Partie 1 : Data Visualisation
1. Exploration des données avec Pandas
2. Résumé statistique et interprétation
3. Scatter matrix des features
4. Réduction de dimensionnalité : PCA et t-SNE

### Partie 2 : Clustering
1. K-Means sur PCA et t-SNE
2. Méthode Elbow pour déterminer K optimal
3. Visualisation des clusters
4. Algorithmes alternatifs :
   - Fuzzy C-Means
   - DBSCAN
   - EM (Gaussian Mixture)
   - Hierarchical Clustering
5. Comparaison des algorithmes (Silhouette Score)

## Outils
- Python, Pandas, Scikit-learn, Matplotlib, Seaborn
- skfuzzy (Fuzzy C-Means)
- scipy (Hierarchical Clustering)
