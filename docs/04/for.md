---
layout: default
title: Boucles `for`
parent: Structures de contrôle de flux
nav_order: 1
permalink: /docs/structures/for
---

# Les boucles `for`
{: .no_toc }
Les boucles `for` sont utilisées pour itérer sur une séquence (liste, tuple, ensemble, dictionnaire, etc.) et exécuter un bloc de code pour chaque élément de la séquence.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Syntaxe
La syntaxe de base d'une boucle `for` en Python est la suivante :
- `element` : variable variable qui contiendra la valeur de l'élément de la séquence à chaque itération.
- `sequence` : séquence sur laquelle nous itérons.
```python
for element in sequence:
    # Code exécuté pour chaque élément de la séquence
    print(element)
```

## Itération sur une liste
```python
# Définir une liste
fruits = ["pomme", "banane", "orange"]

# Boucle `for` sur une liste
for fruit in fruits:
    print(fruit)
```

Résultat :
```
pomme
banane
orange
```

## Itération sur une chaîne de caractères
```python
# Définir une chaîne de caractères
phrase = "Bonjour !"

# Boucle `for` sur une chaîne de caractères
for lettre in phrase:
    print(lettre)
```

Résultat :
```
B
o
n
j
o
u
r

!
```

## Itération sur un dictionnaire
```python
# Définir un dictionnaire
personne = {
    "nom": "Dupont",
    "prenom": "Jean",
    "age": 25
}

# Boucle `for` sur un dictionnaire
for cle, valeur in personne.items():
    print(cle, valeur)
```

Résultat :
```
nom Dupont
prenom Jean
age 25
```

## Sortir d'une boucle `for`
```python
# Définir une liste
fruits = ["pomme", "banane", "orange"]

# Boucle `for` avec une condition de sortie
for fruit in fruits:
    if fruit == "banane":
        break
    print(fruit)
```

Résultat :
```
pomme
```
