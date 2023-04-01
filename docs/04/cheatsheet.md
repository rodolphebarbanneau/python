---
layout: default
title: Cheatsheet
parent: Structures de contrôle de flux
nav_order: 1
permalink: /docs/structures/cheatsheet
---

# Cheatsheet
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Les boucles `for`
Utilisation pour répéter un bloc d'instructions un nombre défini de fois
```python
for i in range(5): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 0 à 4

for i in range(5, 10): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 5 à 9

for i in range(5, 10, 2): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 5 à 9 par pas de 2

for i in range(10, 5, -1): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 10 à 6
```

## Les boucles `while`
Utilisation pour répéter un bloc d'instructions tant qu'une condition est vraie
```python
i = 0 # Initialisation d'une variable
while i < 5: # Boucle `while` tant que la condition est vraie
    print(i) # Afficher les nombres de 0 à 4
    i += 1 # Incrémenter la variable
    
    if i == 3: # Condition
        break # Arrêter la boucle
```

## Les conditions
Utilisation pour exécuter un bloc d'instructions si une condition est vraie
```python
if 1 < 2: # Condition
    print("1 est inférieur à 2") # Afficher le message
elif 1 > 2: # Sinon si
    print("1 est supérieur à 2") # Afficher le message
else: # Sinon
    print("1 est égal à 2") # Afficher le message
```
