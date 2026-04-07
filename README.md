# Analyse des performances d’algorithmes d’optimisation (BBOB)

## Description du projet

Ce projet a pour objectif d’analyser et de comparer les performances d’algorithmes d’optimisation sur des fonctions de benchmark issues de la suite BBOB (Black-Box Optimization Benchmarking).

Le travail est organisé en trois parties :
1. Analyse des runs d’un algorithme sur un seul problème
2. Analyse des runs d’un algorithme sur plusieurs problèmes
3. Comparaison entre plusieurs algorithmes

## Structure du dépôt
BlackBox-Optimization-BBOB/
│
├── README.md
├── code.ipynb
├── resume_problemes_DIM10.csv
├── bbobexp_f2_DIM10.tdat
├── bbobexp_f7_DIM10.tdat
├── bbobexp_f10_DIM10.tdat
├── bbobexp_f15_DIM10.tdat
├── bbobexp_f22_DIM10.tdat
├── BIRMIN/
│ └── data_f*/bbobexp_.tdat
├── RANDOMSEARCH-5-1e7D-Brockhoff/
│ └── data_f/bbobexp_.tdat
└── RS-3_bbob_Brockhoff_Hansen/
└── data_f/bbobexp_*.tdat


- Données pour les parties 1 et 2 :
  - bbobexp_f2_DIM10.tdat
  - bbobexp_f7_DIM10.tdat
  - bbobexp_f10_DIM10.tdat
  - bbobexp_f15_DIM10.tdat
  - bbobexp_f22_DIM10.tdat

- Données pour la partie 3 (multi-algorithmes) :
  - BIRMIN/
    - data_f*/bbobexp_*.tdat
  - RANDOMSEARCH-5-1e7D-Brockhoff/
    - data_f*/bbobexp_*.tdat
  - RS-3_bbob_Brockhoff_Hansen/
    - data_f*/bbobexp_*.tdat

## Problèmes étudiés

Les fonctions analysées sont :
- f2
- f7
- f10
- f15
- f22

Les expériences sont réalisées principalement en dimension 10 et une en dimension 20.

## Algorithmes étudiés

Dans la troisième partie, trois algorithmes sont comparés :
- RANDOMSEARCH-5
- RS-3
- BIRMIN


## Méthodologie

Les fichiers `.tdat` contiennent plusieurs runs séparés par le symbole `%`.

Pour chaque fichier :
- Lecture et séparation des runs
- Extraction des données (nombre d’évaluations et fitness)
- Interpolation sur un axe commun
- Utilisation d’une échelle logarithmique

Analyses réalisées :
- Tracé des courbes de convergence
- Calcul de la moyenne (en log)
- Calcul de la médiane
- Analyse de la variabilité (min/max)


## Résultats

- BIRMIN est l’algorithme le plus performant avec une convergence rapide et stable  
- RS-3 présente des performances intermédiaires  
- RANDOMSEARCH-5 est le moins efficace en raison de son caractère aléatoire
- 

## Fichier de sortie

`resume_problemes_DIM10.csv` contient un résumé des performances :
- moyenne finale
- médiane
- meilleure valeur
- pire valeur


## Environnement

Le projet a été exécuté avec :

- Python 3.11.5
- numpy
- pandas
- matplotlib
- jupyter

Système utilisé : Windows11

## Installation et Execution

- Installer les dépendances :

```bash
pip install numpy pandas matplotlib jupyter

- Executer le script avec le notebook Jupyter:

```bash
jupyter notebook code.ipynb

- Accès au code

Repository GitHub : https://github.com/lasimba/BlackBox-Optimization-BBOB
DOI Zenodo : https://doi.org/10.5281/zenodo.19451846


