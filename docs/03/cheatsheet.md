---
layout: default
title: Cheatsheet
parent: Variables avancées
nav_order: 1
permalink: /docs/variables-advanced/cheatsheet
---

# Cheatsheet
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Listes `list`
Utilisation pour des collections ordonnées d'éléments modifiables.
```python
ma_liste = [1, 2, 2, 3, 3, 3] # Déclaration d'une liste
ma_liste.append(4) # Ajouter un élément à la fin de la liste [1, 2, 2, 3, 3, 3, 4]
ma_liste[0] = 0 # Modifier un élément de la liste [0, 2, 2, 3, 3, 3, 4]
ma_liste.pop() # Supprimer le dernier élément de la liste [0, 2, 2, 3, 3, 3]
print(ma_liste) # Afficher la liste

# Slicing
ma_liste = ma_liste[1:] # Supprimer le premier élément de la liste [2, 2, 3, 3, 3]
ma_liste = ma_liste[:-1] # Supprimer le dernier élément de la liste [2, 2, 3, 3]
ma_liste = ma_liste[1:-1] # Supprimer le premier et le dernier élément de la liste [2, 3, 3]
ma_liste = ma_liste[::2] # Supprimer tous les éléments d'index pairs de la liste [2, 3]
ma_liste = ma_liste[::-1] # Inverser l'ordre des éléments de la liste [3, 2]
print(ma_liste) # Afficher la liste

# Compréhension de liste
ma_liste = [x for x in range(10)] # Créer une liste de 10 éléments de 0 à 9
ma_liste = [x for x in range(10) if x % 2 == 0] # Créer une liste de 5 éléments pairs de 0 à 8
print(ma_liste) # Afficher la liste [0, 2, 4, 6, 8]
```

## Tuples `tuple`
Utilisation pour des collections ordonnées d'éléments immuables.
```python
mon_tuple = (1, 2, 2, 3) # Déclaration d'un tuple
a, b, c, d = mon_tuple # Déballage d'un tuple
mon_tuple[0] # Accès à un élément d'un tuple
mon_tuple[0] = 0 # Erreur : un tuple est immuable
print(a, b, c, d) # Afficher les éléments du tuple (1, 2, 2, 3)
```

## Ensembles `set`
Utilisation pour des collections non-ordonnées d'éléments uniques.
```python
mon_set = {1, 2, 3} # Déclaration d'un ensemble
mon_set.add(4) # Ajouter un élément à l'ensemble
mon_set.add(4) # Ajouter un élément déjà présent à l'ensemble
mon_set.discard(3) # Supprimer un élément de l'ensemble
print(mon_set) # Afficher l'ensemble {1, 2, 4}
```

## Dictionnaires `dict`
Utilisation pour des collections non-ordonnées de paires clé-valeur.
```python
mon_dict = {"cle1": "valeur1", "cle2": "valeur2"} # Déclaration d'un dictionnaire
mon_dict["cle1"] # Accès à une valeur via sa clé
mon_dict["cle3"] = "valeur3" # Ajout d'une paire clé-valeur
del mon_dict["cle2"] # Suppression d'une paire clé-valeur
print(mon_dict) # Afficher le dictionnaire {"cle1": "valeur1", "cle3": "valeur3"}
```
