---
layout: default
title: Ensembles `set`
parent: Variables avancées
nav_order: 4
permalink: /docs/variables-advanced/sets
---

# Les ensembles
{: .no_toc }
En Python, les ensembles (ou sets) sont des collections de données non ordonnées et non indexées. Les ensembles sont représentés par des accolades (`{}`) et peuvent contenir différents types de données, comme des entiers, des chaînes de caractères ou encore des tuples.

Les ensembles ont plusieurs avantages :
- Ils permettent de stocker une collection d'éléments uniques. Cela signifie qu'il n'y aura pas de doublons dans un ensemble.
- Les ensembles offrent des opérations mathématiques comme l'union, l'intersection et la différence qui peuvent être très utiles pour travailler avec des ensembles de données.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Création d'un ensemble
Pour créer un ensemble en Python, on utilise la fonction `set()` ou on peut également déclarer un ensemble vide avec des accolades `{}`. Par exemple :
```python
# Création d'un ensemble à partir d'une liste
mon_ensemble = set([1, 2, 3, 4, 5])
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5}

# Création d'un ensemble vide
mon_ensemble = set()
print(type(mon_ensemble))  # Affiche <class 'set'>
```

On peut également créer un ensemble directement avec des accolades, comme ceci :
```python
# Création d'un ensemble
mon_ensemble = {1, 2, 3, 4, 5}
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5}

# Création d'un ensemble vide
mon_ensemble = {}
print(type(mon_ensemble))  # Affiche <class 'dict'>
```

Les éléments d'un ensemble ne sont pas indexés, donc il n'est pas possible d'accéder à un élément en utilisant un index. Par exemple :
```python
mon_ensemble = {1, 2, 3, 4, 5}
print(mon_ensemble[0])  # Erreur
```

## Accès aux éléments d'un ensemble
Il n'est pas possible d'accéder aux éléments d'un ensemble en utilisant un index. Cependant, il est possible de vérifier si un élément est présent dans un ensemble en utilisant l'opérateur `in`. Par exemple :
```python
mon_ensemble = {1, 2, 3, 4, 5}
print(1 in mon_ensemble)  # Affiche True
print(6 in mon_ensemble)  # Affiche False
```

## Fonctions intégrées pour manipuler les ensembles
Il existe de nombreuses fonctions intégrées en Python qui permettent de manipuler les ensembles, notamment :
- **`len(mon_ensemble)`** : renvoie le nombre d'éléments de l'ensemble `mon_ensemble`.
- **`max(mon_ensemble)`** : renvoie l'élément le plus grand de l'ensemble `mon_ensemble`.
- **`min(mon_ensemble)`** : renvoie l'élément le plus petit de l'ensemble `mon_ensemble`.
- **`sorted(mon_ensemble)`** : renvoie une liste triée des éléments de l'ensemble `mon_ensemble`.
- **`sum(mon_ensemble)`** : renvoie la somme des éléments de l'ensemble `mon_ensemble`.
- **`any(mon_ensemble)`** : renvoie True si au moins un élément de l'ensemble `mon_ensemble` est vrai.
- **`all(mon_ensemble)`** : renvoie True si tous les éléments de l'ensemble `mon_ensemble` sont vrais.
- **`enumerate(mon_ensemble)`** : renvoie un objet enumerate qui peut être utilisé pour parcourir l'ensemble `mon_ensemble`.
- **`zip(mon_ensemble)`** : renvoie un objet zip qui peut être utilisé pour parcourir plusieurs ensembles en même temps.

## Opérations mathématiques sur les ensembles
Les ensembles ont plusieurs opérations mathématiques qui peuvent être très utiles pour travailler avec des ensembles de données. Voici quelques exemples :
```python
# Création de deux ensembles
ensemble1 = {1, 2, 3, 4, 5}
ensemble2 = {4, 5, 6, 7, 8}

# Union
ensemble3 = ensemble1 | ensemble2
print(ensemble3)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}

# Intersection
ensemble3 = ensemble1 & ensemble2
print(ensemble3)  # Affiche {4, 5}

# Différence
ensemble3 = ensemble1 - ensemble2
print(ensemble3)  # Affiche {1, 2, 3}

# Différence symétrique
ensemble3 = ensemble1 ^ ensemble2
print(ensemble3)  # Affiche {1, 2, 3, 6, 7, 8}

# Sous-ensemble
print({1, 2, 3} <= ensemble1)  # Affiche True
print({1, 2, 3} <= ensemble2)  # Affiche False

# Super-ensemble
print(ensemble1 >= {1, 2, 3})  # Affiche True
print(ensemble2 >= {1, 2, 3})  # Affiche False

# Égalité
print({1, 2, 3} == {3, 2, 1})  # Affiche True
print({1, 2, 3} == {1, 2, 3, 4})  # Affiche False

# Inégalité
print({1, 2, 3} != {3, 2, 1})  # Affiche False
print({1, 2, 3} != {1, 2, 3, 4})  # Affiche True

# Égalité stricte
print({1, 2, 3} is {3, 2, 1})  # Affiche False
print({1, 2, 3} is {1, 2, 3})  # Affiche False

# Inégalité stricte
print({1, 2, 3} is not {3, 2, 1})  # Affiche True
print({1, 2, 3} is not {1, 2, 3})  # Affiche True

# Inclusion
print({1, 2, 3} < {1, 2, 3, 4})  # Affiche True
print({1, 2, 3} < {1, 2, 3})  # Affiche False

# Non-inclusion
print({1, 2, 3} > {1, 2, 3, 4})  # Affiche False
print({1, 2, 3} > {1, 2, 3})  # Affiche False
```

## Méthodes courantes de manipulation d'ensembles
Il existe plusieurs méthodes courantes pour manipuler les ensembles en Python. Voici quelques exemples :

### `mon_ensemble.add(x)`
Ajoute un élément `x` à l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Ajout d'un élément à l'ensemble
mon_ensemble.add(6)
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5, 6}
```

### `mon_ensemble.clear()`
Supprime tous les éléments de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de tous les éléments de l'ensemble
mon_ensemble.clear()
print(mon_ensemble)  # Affiche set()
```

### `mon_ensemble.copy()`
Renvoie une copie de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Copie de l'ensemble
mon_ensemble2 = mon_ensemble.copy()
print(mon_ensemble2)  # Affiche {1, 2, 3, 4, 5}
```

### `mon_ensemble.difference(mon_ensemble2)`
Renvoie la différence entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Différence entre les deux ensembles
mon_ensemble3 = mon_ensemble.difference(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3}
```

### `mon_ensemble.difference_update(mon_ensemble2)`
Supprime tous les éléments de l'ensemble qui sont également présents dans l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments communs entre les deux ensembles
mon_ensemble.difference_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3}
```

### `mon_ensemble.discard(x)`
Supprime l'élément `x` de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de l'élément 3 de l'ensemble
mon_ensemble.discard(3)
print(mon_ensemble)  # Affiche {1, 2, 4, 5}
```

### `mon_ensemble.intersection(mon_ensemble2)`
Renvoie l'intersection entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Intersection entre les deux ensembles
mon_ensemble3 = mon_ensemble.intersection(mon_ensemble2)
print(mon_ensemble3)  # Affiche {4, 5}
```

### `mon_ensemble.intersection_update(mon_ensemble2)`
Supprime tous les éléments de l'ensemble qui ne sont pas présents dans l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments qui ne sont pas communs entre les deux ensembles
mon_ensemble.intersection_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {4, 5}
```

### `mon_ensemble.isdisjoint(mon_ensemble2)`
Renvoie `True` si l'ensemble et l'ensemble `mon_ensemble2` ne possèdent aucun élément commun, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'intersection entre les deux ensembles
print(mon_ensemble.isdisjoint(mon_ensemble2))  # Affiche False
```

### `mon_ensemble.issubset(mon_ensemble2)`
Renvoie `True` si l'ensemble est inclus dans l'ensemble `mon_ensemble2`, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'inclusion entre les deux ensembles
print(mon_ensemble.issubset(mon_ensemble2))  # Affiche False
```

### `mon_ensemble.issuperset(mon_ensemble2)`
Renvoie `True` si l'ensemble est inclus dans l'ensemble `mon_ensemble2`, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'inclusion entre les deux ensembles
print(mon_ensemble.issuperset(mon_ensemble2))  # Affiche False
```

### `mon_ensemble.pop()`
Supprime un élément au hasard de l'ensemble et le renvoie :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression d'un élément au hasard de l'ensemble
mon_ensemble.pop()
print(mon_ensemble)  # Affiche {2, 3, 4, 5}
```

### `mon_ensemble.remove(x)`
Supprime l'élément `x` de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de l'élément 3 de l'ensemble
mon_ensemble.remove(3)
print(mon_ensemble)  # Affiche {1, 2, 4, 5}
```

### `mon_ensemble.symmetric_difference(mon_ensemble2)`
Renvoie la différence symétrique entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Différence symétrique entre les deux ensembles
mon_ensemble3 = mon_ensemble.symmetric_difference(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3, 6, 7, 8}
```

### `mon_ensemble.symmetric_difference_update(mon_ensemble2)`
Supprime tous les éléments de l'ensemble qui sont également présents dans l'ensemble `mon_ensemble2` et ajoute tous les éléments de l'ensemble `mon_ensemble2` qui ne sont pas présents dans l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments communs entre les deux ensembles
mon_ensemble.symmetric_difference_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3, 6, 7, 8}
```

### `mon_ensemble.union(mon_ensemble2)`
Renvoie l'union entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Union entre les deux ensembles
mon_ensemble3 = mon_ensemble.union(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}
```

### `mon_ensemble.update(mon_ensemble2)`
Ajoute tous les éléments de l'ensemble `mon_ensemble2` à l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Ajout des éléments de l'ensemble 2 à l'ensemble 1
mon_ensemble.update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}
```

## Boucler sur un ensemble
Il est possible de boucler sur un ensemble en Python grâce à la boucle `for` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Boucle sur l'ensemble
for element in mon_ensemble:
    print(element)
```

## Utilisation avancée des ensembles
Les ensembles en Python peuvent être utilisés pour effectuer des opérations sur des listes ou des chaînes de caractères.

### Suppression des doublons d'une liste
Il est possible de supprimer les doublons d'une liste en utilisant un ensemble :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]

# Suppression des doublons de la liste
ma_liste = list(set(ma_liste))
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

### Suppression des doublons d'une chaîne de caractères
Il est possible de supprimer les doublons d'une chaîne de caractères en utilisant un ensemble :
```python
# Déclaration de la chaîne de caractères
ma_chaine = "Hello World"

# Suppression des doublons de la chaîne de caractères
ma_chaine = "".join(set(ma_chaine))
print(ma_chaine)  # Affiche "Helo Wrd"
```

### Comptage des caractères d'une chaîne de caractères
Il est possible de compter les caractères d'une chaîne de caractères en utilisant un ensemble :
```python
# Déclaration de la chaîne de caractères
ma_chaine = "Hello World"

# Comptage des caractères de la chaîne de caractères
mon_ensemble = set(ma_chaine)
print(len(mon_ensemble))  # Affiche 8
```
