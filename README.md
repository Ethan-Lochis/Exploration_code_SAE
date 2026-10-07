# Lab & Exploration

Un laboratoire de recherche et d'expérimentation technologique sous forme de **monorepo avec Git Submodules**.

Ce dépôt regroupe différents micro-projets servant à découvrir et tester de nouvelles technologies et briques logicielles avant leur intégration dans des projets plus larges.

---

## Philosophie & Approche

> **Comprendre la mécanique plutôt que réinventer la syntaxe.**

Ces explorations sont menées avec l'aide d'outils d'**IA générative**. L'objectif premier n'est pas d'écrire chaque ligne de code à la main, mais de :
-  **Comprendre l'architecture et la logique interne** des outils et librairies explorés.
-  **Tester la faisabilité et les limites** d'une approche technique rapidement.
-  **Valider des cas d'usage réels** pour alimenter des projets plus matures.
-  **Développer une vision système** : flux de données, intégration d'API, contraintes de performance et d'expérience utilisateur.

---

##  Modules & Projets

Chaque projet est maintenu dans son propre sous-module Git afin de préserver son cycle de vie, son historique indépendant et la gestion fine de ses accès :

| Dossier | Description / Cible | Dépôt source |
| :--- | :--- | :--- |
| [`Chatbot/`](file:///c:/Users/ethan/Documents/CODE/Exploration/Chatbot) | Expérimentations de flux conversationnels, intégration d'API LLM et logique d'assistance IA | [Ethan-Lochis/IA-feytiat-tests](https://github.com/Ethan-Lochis/IA-feytiat-tests) |
| [`leaflet/`](file:///c:/Users/ethan/Documents/CODE/Exploration/leaflet) | Exploration cartographique interactive avec la librairie Leaflet (couches, géolocalisation, markers) | [Ethan-Lochis/Leaflet](https://github.com/Ethan-Lochis/Leaflet) |

---

## Prise en main

### Cloner ce dépôt et initialiser tous les sous-modules

Pour récupérer l'ensemble des projets en une seule étape :

```bash
git clone --recurse-submodules https://github.com/<votre-compte>/Exploration.git
```

Si le dépôt principal a déjà été cloné sans les sous-modules :

```bash
git submodule update --init --recursive
```

> [!NOTE]
> Certains sous-modules peuvent être hébergés sur des dépôts privés. Assurez-vous d'avoir les droits d'accès correspondants sur GitHub pour les cloner localement.

---

## Gestion des sous-modules au quotidien

### Mettre à jour tous les sous-modules avec leur dernière version
```bash
git submodule update --remote --merge
```

### Ajouter une nouvelle exploration
```bash
git submodule add https://github.com/<compte>/<nouveau-projet>.git <nom-dossier>
git commit -m "feat: ajout du submodule <nom-dossier>"
```
