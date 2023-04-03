---
layout: default
title: Fonctions callback
parent: Fonctions
nav_order: 4
permalink: /docs/functions/callback
---

# Les fonctions callback
{: .no_toc }
Les fonctions callback sont des fonctions qui sont passées en paramètre d'une autre fonction. Elle sont souvent utilisées pour exécuter du code après l'exécution d'une autre fonction.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Définition d'une fonction avec callback
Une fonction avec callback est définie comme une fonction standard avec le mot clé `def` suivi du nom de la fonction, des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction callback
def nom_fonction_callback():
    print("Je suis une fonction callback")

# Définition d'une fonction avec une fonction callback en paramètre
def nom_fonction(parametre1, parametre2, callback):
    # Code exécuté par la fonction
    print(parametre1 + parametre2)
    callback()

# Appel d'une fonction avec une fonction callback en paramètre
nom_fonction(2, 3, nom_fonction_callback) # Affiche 5 puis "Je suis une fonction callback"
```

## Appel d'une fonction avec callback
Une fonction avec callback est appelée comme une fonction standard.
```python
# Appel d'une fonction avec callback
nom_fonction(parametre1, parametre2, nom_fonction_callback)
```
