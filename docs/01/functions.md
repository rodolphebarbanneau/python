---
layout: default
title: Les fonctions
parent: Concepts de base de la programmation
nav_order: 4
---

# Les fonctions

## Définition d'une fonction
Une fonction est un bloc de code qui exécute une tâche spécifique. En Python, vous pouvez définir une fonction comme ceci :
```python
def nom_fonction(parametre1, parametre2):
    # Code exécuté par la fonction
    print(parametre1 + parametre2)
```

## Appel d'une fonction

Une fonction est appelée en utilisant son nom suivi de parenthèses :
```python
nom_fonction(parametre1, parametre2)
```

## Fonctions natives
Python possède de nombreuses fonctions natives qui peuvent être utilisées pour effectuer des tâches courantes. Parmi les fonctions natives les plus courantes, nous retrouvons :

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `print()` | Affiche un message à l'écran | `print("Hello World")` |
| `input()` | Demande à l'utilisateur d'entrer une valeur | `input("Entrez une valeur : ")` |
| `type()` | Retourne le type d'une variable | `type(2)` |
| `int()` | Convertit une valeur en nombre entier | `int('2')` |
| `float()` | Convertit une valeur en nombre à virgule flottante | `float('2.5')` |
| `str()` | Convertit une valeur en chaîne de caractères | `str(2)` |
| `bool()` | Convertit une valeur en booléen | `bool(1)` |
| `datetime()` | Convertit une valeur en date et heure | `datetime(2020, 1, 1)` |
| `round()` | Arrondit un nombre à un nombre de décimales donné | `round(2.5)` |
| `abs()` | Retourne la valeur absolue d'un nombre | `abs(-2)` |
| `pow()` | Retourne la puissance | `pow(2, 3)` |
| `help()` | Affiche l'aide d'une fonction | `help(print)` |
