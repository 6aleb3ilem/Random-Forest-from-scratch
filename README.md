
#  Projet ML: Prédiction des Valeurs Commerciales des Produits de Pêche en Afrique


---

## Objectif
Ce projet vise à prédire les valeurs commerciales des produits de pêche (poissons et crustacés) en Afrique à l'aide d'un modèle Random Forest construit de zéro. Le dataset `Africa_Value.csv` couvre 57 pays de 2000 à 2015.

---

## Spécifications Techniques
- **Dataset** : `Africa_Value.csv` (valeurs en $US).
- **Features** : Pays, flux (export/import), produit, année relative, valeur précédente, moyenne mobile 3 ans.
- **Entraînement** : 2000-2012
## Données
- **217 observations** (57 pays africains)
- **Période** : 2000-2015
- **Produits** : Poissons et Crustacés
- **Types** : Exportations et Importations

## Méthode
- **Algorithme** : Random Forest (50 arbres)
- **Features** : 6 variables incluant pays, produit, année, valeurs historiques
- **Entraînement** : 2000-2012
- **Test** : 2013-2015

---

## Résultats
- **Métriques** :
 - **R² = 0.9784** (explique 97.84% de la variance)
- **MAE = $6,319.65** (erreur moyenne)
- **RMSE = $20,171.78**
- **Prédictions 2016 (Top 5)** :
  - Nigeria - Import - Fish : $966,394.54
  - Maroc - Export - Fish : $951,921.42
  - Namibie - Export - Fish : $767,758.83
  - Égypte - Import - Fish : $716,447.73
  - Seychelles - Export - Fish : $465,996.

### Performance par Catégorie
| Type | MAE |
|------|-----|
| Exportations | $6,612.22 |
| Importations | $6,050.39 |
| Poissons | $10,586.52 |
| Crustacés | $1,597.10 |

## Visualisations


### Prédictions vs Réalité
![im1](https://github.com/user-attachments/assets/e0064f9b-d11d-4e90-8435-fb69afe7e600)

- Points suivent bien la ligne rouge
- Bonnes prédictions sauf valeurs très élevées

### Performance par Pays
![im2](https://github.com/user-attachments/assets/e50d49bc-5c7f-409f-b4c8-e0a1dd0cd121)

- **Meilleurs** : Guinée-Bissau, Éthiopie, Djibouti
- **Moins bons** : Nigeria, Namibie, Seychelles

### Distribution des Erreurs
![im3](https://github.com/user-attachments/assets/81bc01d3-403e-4e46-9a71-b7e0e94bcc60)

- Majorité des erreurs proche de zéro
- Quelques cas extrêmes sur petites valeurs
## Prédictions 2016
- **Total Exportations** : $4,944,132
- **Total Importations** : $5,806,303
- **Top 3 pays** : Nigeria, Maroc, Namibie
---

---

## Insights
- Les features temporelles (moyenne mobile, valeur précédente) dominent les prédictions.
- Le modèle est plus précis pour les crustacés que pour les poissons.
- Certains pays (ex. Nigeria) ont des erreurs plus élevées en raison de grandes valeurs.
- Modèle très performant (R² > 0.97)  
- Implémentation complète sans librairies ML  


---


---

## Livrables
- **Notebook** : [Lien vers Google Colab](https://colab.research.google.com/drive/1DMIx6J0Rf52-nmQT6nuaI32qTZ9RiPJU?usp=sharing)

---

## Conclusion
Le modèle atteint un R² de 0.9627, démontrant une bonne capacité prédictive. Ce projet illustre un apprentissage pratique du machine learning depuis zéro, avec des améliorations possibles pour les grandes valeurs.
