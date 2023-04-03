---
layout: default
title: Fonctions récursives
parent: Fonctions
nav_order: 4
permalink: /docs/functions/recursion
---

# Les fonctions récursives
{: .no_toc }
Les fonctions récursives sont des fonctions qui s'appellent elles-mêmes. Elles sont utilisées pour résoudre des problèmes qui peuvent être découpés en sous-problèmes similaires. Elles doivent avoir une condition d'arrêt pour éviter une boucle infinie.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Définition d'une fonction récursive
Une fonction récursive est définie comme une fonction standard avec le mot clé `def` suivi du nom de la fonction, des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction récursive
def nom_fonction(parametre1, parametre2):
    # Code exécuté par la fonction
    if condition:
        # Récursion si la condition est vraie
        return nom_fonction(parametre1, parametre2)
    else:
        # Code exécuté si la condition est fausse (condition d'arrêt)
        return resultat
```

## Appel d'une fonction récursive
Une fonction récursive est appelée comme une fonction standard.
```python
# Appel d'une fonction récursive
nom_fonction(parametre1, parametre2)
```
