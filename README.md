# Mini-Projet N°1 — Médias Sociaux & Santé Mentale

> **INSSEDS** · Institut Supérieur de Statistique, d'Économétrie et de Data Science  
> Master 2 : Statistique – Économétrie – Data Science · Année académique 2025-2026  
> Encadré par : **YAO Kouakou Jean Martinien** · Encadreur : **AKPOSSO Didier Martial**

---

## Description

Analyse inférentielle de l'impact des médias sociaux sur le bien-être psychologique d'un échantillon de **500 utilisateurs indiens**. L'étude examine les relations entre le temps d'écran, la qualité du sommeil, le genre, l'exercice physique, la plateforme utilisée et le bien-être mesuré par le niveau de stress et l'indice de bonheur.

---

## Structure du rapport

```
├── 1. Introduction & problématique
├── 2. Données & méthodologie
├── 3. Résultats (H1 à H6)
├── 4. Discussion
├── 5. Conclusion & recommandations
└── Annexe — Code source Python
```

---

## Données

| Paramètre | Valeur |
|---|---|
| Fichier | `sante_mental_media_sociaux.csv` |
| Taille de l'échantillon | n = 500 |
| Valeurs manquantes | Aucune |
| Origine | Inde |
| Variables | 10 (démographiques, numériques, bien-être) |

---

## Méthodes statistiques

- Corrélation de Pearson
- Test t de Student (avec test de Levene préalable)
- ANOVA à un facteur (one-way ANOVA)
- Intervalles de confiance à 95 %
- Winsorisation (règle de Tukey)

---

## Résultats des hypothèses

| Hypothèse | Test | Statistique | p-value | Verdict |
|---|---|---|---|---|
| H1 : Temps d'écran → stress | Pearson | r = 0,740 | < 0,001 | ✅ Confirmée |
| H2 : Qualité sommeil → bonheur | Pearson | r = 0,679 | < 0,001 | ✅ Confirmée |
| H3 : Genre → stress différent | Test t | t = 0,215 | 0,830 | ❌ Rejetée |
| H4 : Exercice → stress/bonheur | Pearson | r = −0,019 / 0,041 | 0,678 / 0,358 | ❌ Rejetée |
| H5 : Plateforme → stress/bonheur | ANOVA | F = 1,13 / 1,73 | 0,342 / 0,127 | ❌ Rejetée |
| H6 : Jours sans RS → stress/bonheur | Pearson | r = −0,008 / 0,064 | 0,859 / 0,156 | ❌ Rejetée |

---

## Enseignements clés

- Le **temps d'écran** est le principal facteur numérique associé à l'augmentation du stress (r = 0,74).
- La **qualité du sommeil** est le principal déterminant comportemental du bonheur (r = 0,68).
- Le genre, la plateforme, l'exercice et le sevrage numérique ne montrent pas d'association significative.

---

## Installation

```bash
pip install pandas numpy scipy matplotlib
```

## Utilisation

```bash
python analyse_statistique.py      # Analyses principales + graphiques
python nuages_objectif6.py         # Nuages de points — Objectif 6
```

---

## Références

- Andreassen & Pallesen (2014) — *Social network site addiction*
- Cain & Gradisar (2010) — *Electronic media use and sleep*
- Primack et al. (2017) — *Social media use and perceived social isolation*
- Twenge (2017) — *iGen*
