---
layout: default
title: Structures de contrôle de flux
parent: Concepts de base
nav_order: 3
permalink: /docs/concepts/stuctures
---

# Les structures de contrôle de flux
Les structures de contrôle de flux sont utilisées pour décider de l'exécution ou non d'une partie de votre code. Les structures de contrôle de flux courantes en Python sont :
- Les instructions `if`/`elif`/`else` :
```python
if condition1:
    # Code exécuté si la condition1 est vraie
    print("La condition est vraie")
elif condition2:
    # Code exécuté si la condition2 est vraie
    print("La condition2 est vraie")
else:
    # Code exécuté si les conditions sont fausses
    print("Les conditions sont fausses")
```
- Les boucles `for` :
```python
for element in sequence:
    # Code exécuté pour chaque élément de la séquence
    print(element)
```
- Les boucles `while` :
```python
while condition:
    # Code exécuté tant que la condition est vraie
    print("La condition est vraie")
```

- Les instructions `try`/`except` :
```python
try:
    # Code exécuté
    print("Le code est exécuté")
except:
    # Code exécuté si une erreur est survenue
    print("Une erreur est survenue")
```
