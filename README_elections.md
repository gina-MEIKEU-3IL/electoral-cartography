# 🗳️ Étude du Comportement Électoral à l'Échelle Infra-Communale

> Projet académique Big Data Challenge — 3IL Ingénieurs | Client : INSEE

---

## 📌 Contexte et objectif

Ce projet analyse les résultats des élections présidentielles françaises à différentes échelles géographiques (région, département, commune) en les croisant avec les caractéristiques sociodémographiques des électeurs (âge, revenu, catégorie socioprofessionnelle) issues de l'INSEE.

**Objectif :** Créer une cartographie interactive accessible à tous les citoyens pour comprendre les comportements électoraux sur le territoire français.

---

## 🗂️ Structure du projet

```
electoral-cartography/
│
├── data/
│   ├── resultats_presidentielles_2022.csv     # Résultats électoraux (data.gouv.fr)
│   └── donnees_sociodemographiques_insee.csv  # Données INSEE par département
│
├── electoral_analysis.ipynb    # Notebook principal (pipeline complet)
├── results_elections_powerbi.csv              # Export pour Power BI
├── requirements.txt            # Dépendances Python
└── README.md                   # Documentation du projet
```

---

## 📥 Sources de données

| Source | Données | Lien |
|--------|---------|------|
| Ministère de l'Intérieur | Résultats électoraux Présidentielle 2022 | [data.gouv.fr](https://www.data.gouv.fr/fr/datasets/election-presidentielle-des-10-et-24-avril-2022-resultats-definitifs-du-1er-tour/) |
| INSEE | Données sociodémographiques par département | [insee.fr](https://www.insee.fr/fr/statistiques) |

---

## 🔄 Pipeline du projet

```
Collecte Open Data  →  Nettoyage  →  Analyse exploratoire  →  Croisement sociodémographique  →  Visualisation  →  Export Power BI
```

### 1. Collecte des données
- Résultats de l'élection présidentielle 2022 (1er tour) par département
- Données sociodémographiques INSEE : âge, revenus, catégorie socioprofessionnelle

### 2. Nettoyage et préparation
- Correction des valeurs manquantes et des doublons
- Harmonisation des clés de jointure (codes département)
- Calcul des taux de participation et d'abstention par département

### 3. Analyse exploratoire (EDA)
- Distribution du taux de participation par département
- Identification des territoires à forte/faible mobilisation
- Statistiques descriptives (moyenne, min, max, distribution)

### 4. Croisement données électorales × sociodémographie
- Fusion des datasets sur le code département
- Analyse des corrélations entre comportement électoral et caractéristiques des territoires
- Identification des facteurs influençant la participation (âge, revenus, CSP)

### 5. Visualisations
- Top/Flop départements par taux de participation
- Distribution de la participation sur le territoire
- Corrélations entre variables sociodémographiques et résultats électoraux

### 6. Export pour Power BI
- Dashboard interactif avec filtres par région, département et période
- KPI : taux de participation, abstention, répartition des voix

---

## 📊 Principaux résultats

| Indicateur | Valeur |
|-----------|--------|
| Taux de participation moyen | ~73 % |
| Département le plus mobilisé | Lozère |
| Département le moins mobilisé | Seine-Saint-Denis |
| Corrélation revenu / participation | Positive |

**Enseignements clés :**
- Les territoires à revenus élevés présentent des taux de participation plus importants
- Les jeunes électeurs sont sous-représentés dans les zones urbaines denses
- L'abstention est structurellement plus élevée dans les DOM-TOM

---

## 🛠️ Stack technique

| Outil | Usage |
|-------|-------|
| Python 3 | Langage principal |
| Pandas | Collecte, nettoyage et manipulation des données |
| Matplotlib / Seaborn | Visualisations et analyses graphiques |
| Power BI (DAX, Power Query) | Dashboard interactif de cartographie |
| Git / GitHub | Versioning et partage du projet |

---

## ⚙️ Installation et exécution

```bash
# Cloner le repository
git clone https://github.com/gina-MEIKEU-3IL/electoral-cartography.git
cd electoral-cartography

# Installer les dépendances
pip install -r requirements.txt

# Télécharger les données (voir liens ci-dessus) et les placer dans data/

# Lancer le notebook
jupyter lab electoral_analysis.ipynb
```

---

## 🏫 Contexte académique

- **Établissement :** 3IL Ingénieurs, Limoges
- **Module :** Big Data Challenge
- **Client :** INSEE (Institut National de la Statistique et des Études Économiques)
- **Méthodologie :** Agile Scrum — 5 sprints sur 10 semaines
- **Équipe :** 4 développeurs

---

## 👩‍💻 Auteure

**Gina Beguele TSAGA MEIKEU**  
Étudiante ingénieure — spécialisation Data, BI & IA  
3IL Ingénieurs, Limoges  
📧 meikeuginabeguele@gmail.com  
🔗 github.com/gina-MEIKEU-3IL
