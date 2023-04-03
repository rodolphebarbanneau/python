---
layout: default
title: Paramètres et arguments
parent: Fonctions
nav_order: 3
permalink: /docs/functions/parameters
---

# Les paramètres et les arguments des fonctions
{: .no_toc }
Les paramètres et les arguments sont des notions très importantes en programmation. Ils permettent de rendre les fonctions plus flexibles et plus réutilisables. Les paramètres sont les variables qui sont définies dans la fonction. Les arguments sont les valeurs qui sont passées à la fonction lors de son appel.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Les paramètres standards
Les paramètres sont des variables utilisées à l'intérieur d'une fonction pour stocker des valeurs. Les paramètres sont spécifiés dans la définition de la fonction, entre les parenthèses `()` après le nom de la fonction. Voici un exemple de définition d'une fonction avec des paramètres :
```python
# Addition de 2 nombres a et b
def addition(a, b):
    resultat = a + b
    print(resultat) # Affiche le résultat de l'addition
```

Dans cet exemple, la fonction `addition()` prend deux paramètres, `a` et `b`, qui sont utilisés pour effectuer l'addition.

## Les paramètres par défaut ou optionnels
Il est possible de spécifier une valeur par défaut pour un paramètre de fonction en utilisant le signe `=`. Ainsi, si aucun argument n'est passé pour ce paramètre lors de l'appel de la fonction, sa valeur par défaut sera utilisée. Voici un exemple :
```python
# Fonction qui affiche un message de salutation
def saluer(nom=""):
    if nom:
        print("Bonjour, " + nom + " !")
    else:
        print("Bonjour !")
```

Dans cet exemple, la fonction `saluer()` prend un paramètre `nom`, avec une valeur par défaut vide. Si le paramètre `nom` est spécifié lors de l'appel de la fonction, la valeur du paramètre sera utilisée. Sinon, la valeur par défaut sera utilisée.

## Les paramètres indéfinis

### Sous forme de tuple `*args`
Il est possible de spécifier un nombre indéfini de paramètres pour une fonction en utilisant le caractère `*` avant le nom du paramètre. On utilise souvent le nom `args` pour désigner ce type de paramètre. Voici un exemple :
```python
# Fonction qui affiche un message de salutation
def saluer(*noms):
    for nom in noms:
        print("Bonjour, " + nom + " !")

# Appel de la fonction avec un nombre indéfini de paramètres
saluer("Alice", "Bob", "Charlie")
```

Dans cet exemple, la fonction `saluer()` prend un nombre indéfini de paramètres, `noms`, qui sont utilisés pour afficher un message de salutation pour chaque nom :
```
Bonjour, Alice !
Bonjour, Bob !
Bonjour, Charlie !
```

### Sous forme de dictionnaire `**kwargs` (paramètres nommés)
Il est possible de spécifier un nombre indéfini de paramètres nommés pour une fonction en utilisant le caractère `**` avant le nom du paramètre. On utilise souvent le nom `kwargs` pour désigner ce type de paramètre. Voici un exemple :
```python
# Fonction qui affiche un message de salutation
def saluer(**noms):
    for nom in noms:
        print("Bonjour, " + nom.value() + " !")

# Appel de la fonction avec un nombre indéfini de paramètres nommés
saluer(nom1="Alice", nom2="Bob", nom3="Charlie")
```

Dans cet exemple, la fonction `saluer()` prend un nombre indéfini de paramètres nommés, `noms`, qui sont utilisés pour afficher un message de salutation pour chaque nom :
```
Bonjour, Alice !
Bonjour, Bob !
Bonjour, Charlie !
```

## Les arguments des fonctions
Les arguments sont des valeurs que l'on passe à une fonction lorsque nous l'appelons. Les arguments sont spécifiés entre les parenthèses `()` après le nom de la fonction lors de l'appel de la fonction. Voici un exemple d'appel de la fonction `addition()` :
```python
addition(2, 3) # Affiche 5
```

Dans cet exemple, la fonction `addition()` est appelée avec les arguments `2` et `3`.

## Les arguments nommés
Il est possible de passer des arguments à une fonction en utilisant le nom du paramètre. Voici un exemple :
```python
# Fonction qui affiche un message de salutation
def saluer(nom=""):
    if nom:
        print("Bonjour, " + nom + " !")
    else:
        print("Bonjour !")

saluer(nom="John") # Affiche "Bonjour, John !"
```
