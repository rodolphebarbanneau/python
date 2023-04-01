---
layout: default
title: Boucles `while`
parent: Structures de contrôle de flux
nav_order: 3
permalink: /docs/structures/while
---

# Les boucles `while`
{: .no_toc }
Les boucles `while` sont utilisées pour exécuter un bloc de code tant qu'une condition est vraie.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Syntaxe
La syntaxe de base d'une boucle `while` en Python est la suivante :
- `condition` : condition à vérifier à chaque itération.
```python
while condition:
    # Code exécuté tant que la condition est vraie
```

## Boucle `while` avec un compteur
```python
# Initialisation d'une variable
compteur = 0

# Boucle `while` avec un compteur
while compteur < 5:
    print(i)
    compteur += 1
```

Résultat :
```
0
1
2
3
4
```

## Boucle `while` avec une condition de sortie
```python
# Initialisation d'une variable
valeur = ""

# Boucle `while` avec une condition de sortie
while valeur != "q":
    valeur = input("Entrez une valeur (q pour quitter) : ")
    print("Vous avez entré la valeur", valeur)
```

Résultat :
```
Entrez une valeur (q pour quitter) : 1
Vous avez entré la valeur 1
Entrez une valeur (q pour quitter) : 2
Vous avez entré la valeur 2
Entrez une valeur (q pour quitter) : q
Vous avez entré la valeur q
```

## Boucle `while` avec une condition de sortie et une condition de saut
```python
# Initialisation d'une variable
valeur = ""

# Boucle `while` avec une condition de sortie et une condition de saut
while valeur != "q":
    valeur = input("Entrez une valeur (q pour quitter) : ")
    if valeur == "q":
        break
    print("Vous avez entré la valeur", valeur)
```

Résultat :
```
Entrez une valeur (q pour quitter) : 1
Vous avez entré la valeur 1
Entrez une valeur (q pour quitter) : 2
Vous avez entré la valeur 2
Entrez une valeur (q pour quitter) : q
```
