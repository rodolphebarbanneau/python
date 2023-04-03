---
layout: default
title: Introduction
parent: Fonctions
nav_order: 2
permalink: /docs/functions/introduction
---

# Introduction
{: .no_toc }
Les fonctions sont des blocs de code qui effectuent une tâche spécifique. Elles peuvent être utilisées pour effectuer une tâche complexe en divisant le code en blocs plus petits et plus facilement gérables. Les fonctions peuvent également être réutilisées plusieurs fois dans un programme.

En Python, une fonction est définie à l'aide du mot-clé `def`, suivi du nom de la fonction et de ses paramètres entre parenthèses. Le code de la fonction est ensuite écrit entre deux points `:`.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Définition d'une fonction
Une fonction simple est définie avec le mot clé `def` suivi du nom de la fonction, des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction avec 2 paramètres obligatoires et 1 paramètre optionnel
def nom_fonction(parametre1, parametre2, parametre3 = 0):
    # Code exécuté par la fonction
    print(parametre1 + parametre2 + parametre3)

# Définition d'une fonction avec valeur de retour
def somme(parametre1, parametre2):
    # Code exécuté par la fonction
    return parametre1 + parametre2
```

Dans l'exemple ci-dessus, la fonction `nom_fonction` prend 3 paramètres. Le premier et le deuxième paramètre sont obligatoires, le troisième est optionnel. Si le troisième paramètre n'est pas spécifié, il prend la valeur par défaut `0`. La fonction `somme` prend 2 paramètres obligatoires et retourne la somme des deux paramètres.

## Appel d'une fonction
Une fonction est appelée en écrivant son nom suivi de ses paramètres entre `()`.
```python
# Appel d'une fonction sans spécifier les paramètres optionnels
nom_fonction(parametre1, parametre2)

# Appel d'une fonction en spécifiant les paramètres optionnels
nom_fonction(parametre1, parametre2, parametre3)
```
