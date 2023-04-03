---
layout: default
title: Fonctions lambda
parent: Fonctions
nav_order: 5
permalink: /docs/functions/lambda
---

# Les fonctions anonymes ou lambda
{: .no_toc }
Les fonctions anonymes ou lambda sont des fonctions qui ne sont pas définies avec le mot clé `def` mais avec le mot clé `lambda`. Elles sont souvent utilisées pour passer une fonction en paramètre d'une autre fonction.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Définition d'une fonction lambda
Une fonction lambda est définie avec le mot clé `lambda` suivi des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction lambda
nom_lambda = lambda parametre1, parametre2: parametre1 + parametre2

# Utilisation d'une fonction lambda comme callback
def nom_fonction(parametre1, parametre2, callback):
    print(callback())
```

## Appel d'une fonction lambda
Une fonction lambda est appelée comme une fonction standard.
```python
# Appel d'une fonction lambda
nom_lambda(parametre1, parametre2)

# Appel d'une fonction avec une fonction lambda en paramètre
nom_fonction(2, 3, lambda x, y: x + y) # Affiche 5
```
