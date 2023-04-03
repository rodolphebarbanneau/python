---
layout: default
title: Cheatsheet
parent: Fonctions
nav_order: 1
permalink: /docs/functions/cheatsheet
---

# Cheatsheet
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Fonction standard

### Définition d'une fonction
Une fonction est définie avec le mot clé `def` suivi du nom de la fonction, des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction avec 2 paramètres obligatoires et 1 paramètre optionnel
def nom_fonction(parametre1, parametre2, parametre3 = 0):
    # Code exécuté par la fonction
    print(parametre1 + parametre2 + parametre3)

# Appel d'une fonction sans spécifier les paramètres optionnels
nom_fonction(2, 1) # Affiche 3

# Appel d'une fonction en spécifiant les paramètres optionnels
nom_fonction(2, 1, 1) # Affiche 4
```
```python
# Définition d'une fonction avec valeur de retour
def somme(parametre1, parametre2):
    # Code exécuté par la fonction
    return parametre1 + parametre2

# Appel d'une fonction avec valeur de retour
resultat = somme(3, 5) # Resultat vaut 8
```

### Définition d'une fonction avec `*args` et `**kwargs`
Ce sont des paramètres optionnels, ils permettent de récupérer un nombre indéfini de paramètres :
- `*args` : permet de récupérer un nombre indéfini de paramètres sous forme de **tuple**.

```python
# Fonction avec *args (tuple)
def nom_fonction_args(*args):
    # Code exécuté par la fonction
    print(args)

# Appel d'une fonction avec *args
nom_fonction_args(1, 2, 3) # Affiche (1, 2, 3)
```

- `**kwargs` : permet de récupérer un nombre indéfini de paramètres sous forme de **dictionnaire**, on les appelle aussi paramètres nommés.

```python
# Fonction avec **kwargs (dict)
def nom_fonction_kwargs(**kwargs):
    # Code exécuté par la fonction
    print(kwargs)

# Appel d'une fonction avec **kwargs
nom_fonction_kwargs(a=1, b=2, c=3) # Affiche {'a': 1, 'b': 2, 'c': 3}
```

## Fonctions récursives
Une fonction récursive est une fonction qui s'appelle elle-même. Elle est utilisée pour résoudre des problèmes qui peuvent être découpés en sous-problèmes similaires. Elle doit avoir une condition d'arrêt pour éviter une boucle infinie.
```python
# Définition d'une fonction récursive
def factorielle(n):
    if n == 0:
        return 1
    else:
        return n * factorielle(n - 1)

# Appel d'une fonction récursive
resultat = factorielle(5)
print(resultat) # Affiche 120
```

## Fonctions avec callback
Une fonction avec callback est une fonction qui est passée en paramètre d'une autre fonction. Elle est souvent utilisée pour exécuter du code après l'exécution d'une autre fonction.
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

## Fonctions anonymes ou lambda
Une fonction anonyme est une fonction qui n'a pas de nom, elle est définie par une expression lambda. Elle est utilisée pour créer des fonctions simples et courtes. Elle est définie avec le mot clé `lambda` suivi des paramètres (optionnels ou non) et du caractère `:`. Le code de la fonction doit être indenté.
```python
# Définition d'une fonction lambda
somme = lambda x, y: x + y

# Appel de la fonction lambda
resultat = somme(2, 3)
print(resultat) # Affiche 5
```
