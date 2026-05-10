# Post-Processeur Multiaxes — Machine Hitachi-Seiki 5 Axes

**Cours :** SYS856 – Fabrication Assistée par Ordinateur (FAO)  
**Institution :** École de Technologie Supérieure (ÉTS Montréal)  
**Session :** Automne 2024  
**Niveau :** Maîtrise
**Résultat obtenu :** 96/100
**Auteur :** Alae Zerrouq

---

## Contexte

Ce projet a été réalisé dans le cadre du cours SYS856 à l'ÉTS Montréal. L'objectif est de développer un **post-processeur multiaxes** pour une machine CNC Hitachi-Seiki 5 axes à l'aide du logiciel **CAM-POST**.

Un post-processeur est un programme qui traduit les trajectoires d'outil générées par un logiciel FAO (fichiers CL/NCL) en code machine (fichiers TAP) spécifique à une machine-outil donnée, en tenant compte de ses caractéristiques cinématiques et de ses contraintes d'usinage.

---

## Objectifs

- Développer et valider des **macros avancées** pour optimiser les cycles d'usinage en environnement 5 axes
- Implémenter un **cycle spécial pour l'usinage de cavités** conforme aux spécifications industrielles
- Analyser et traiter des fichiers **CL et TAP** pour garantir la conformité aux exigences techniques
- Gérer les **exceptions** et cas particuliers en environnement multiaxe

---

## Structure du projet

```
├── Fichiers_projet/
│   ├── f3axes.ncl              # Fichier CL pour usinage 3 axes
│   ├── f3axes.tap              # Code machine généré (3 axes)
│   ├── f3axes.lst              # Listing de sortie (3 axes)
│   ├── f5axes.ncl              # Fichier CL pour usinage 5 axes
│   ├── f5axes.tap              # Code machine généré (5 axes)
│   ├── f5axes.lst              # Listing de sortie (5 axes)
│   ├── fmotsPP-4.tap           # Code machine avec mots post-processeur
│   ├── fmotsPP-4.lst           # Listing correspondant
│   └── ...                     # Fichiers de test et validation
├── ZERA03.dbf                  # Base de données du post-processeur
├── rapport.pdf                 # Rapport complet du projet
└── README.md
```

---

## Technologies & Outils

| Outil | Usage |
|---|---|
| **CAM-POST** | Développement du post-processeur |
| **Pro/ENGINEER (Creo)** | Génération des fichiers NCL/CL |
| **Hitachi-Seiki 5 axes** | Machine cible |
| **Langage CAMPOST** | Macros et logique du post-processeur |

---

## Résultats

- Post-processeur fonctionnel pour usinage **3 et 5 axes**
- Génération correcte du code G/M machine (fichiers TAP)
- Cycle spécial d'usinage de cavités implémenté et validé
- Gestion des transitions d'axes, des vitesses d'avance et des corrections d'outil

---

## Rapport

Le rapport complet détaillant la méthodologie, les macros développées et les résultats obtenus est disponible dans ce repo : [`rapport.pdf`](./rapport.pdf)
