---
layout: default
title: Listes `list`
parent: Variables avancées
nav_order: 1
permalink: /docs/variables-advanced/lists
---

# Les listes
{: .no_toc }
En Python, une liste est une collection ordonnée d'éléments, pouvant être de différents types (nombres, chaînes de caractères, booléens, autres listes, etc.). Les éléments d'une liste sont séparés par des virgules et encadrés par des crochets `[ ]`.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Création d'une liste
En Python, la syntaxe pour déclarer une liste est la suivante :
```python
nom_liste = [element1, element2, ..., elementN]
```

Voici quelques exemples de déclaration de listes en Python :
```python
# Déclaration d'une liste d'entiers
liste1 = [1, 2, 3, 4, 5]

# Déclaration d'une liste de chaînes de caractères
liste2 = ["Hello", "World", "!"]

# Déclaration d'une liste mixte
liste3 = [1, "Hello", 3.14, True]
```

## Accès aux éléments d'une liste
Pour accéder à un élément particulier d'une liste, vous pouvez utiliser son index. L'index est un nombre entier qui indique la position de l'élément dans la liste, en commençant par 0 pour le premier élément.

Voici un exemple d'accès aux éléments d'une liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Accès à un élément particulier de la liste
print(ma_liste[0])   # Affiche 1
print(ma_liste[2])   # Affiche 3
print(ma_liste[-1])  # Affiche 5
```

Dans cet exemple, nous avons déclaré une liste `ma_liste` et nous avons accédé à certains de ses éléments en utilisant leur index.

## Fonctions intégrées pour manipuler les listes
Il existe de nombreuses fonctions intégrées en Python qui permettent de manipuler les listes, notamment :
- **`len(ma_liste)`** : retourne le nombre d'éléments de la liste `ma_liste`.
- **`sum(ma_liste)`** : retourne la somme des éléments de la liste `ma_liste`.
- **`min(ma_liste)`** : retourne le plus petit élément de la liste `ma_liste`.
- **`max(ma_liste)`** : retourne le plus grand élément de la liste `ma_liste`.
- **`sorted(ma_liste)`** : retourne une copie triée de la liste `ma_liste`.

Voici quelques exemples d'utilisation de ces fonctions :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Fonction intégrée `len()`
print(len(ma_liste))  # Affiche 5

# Fonction intégrée `sum()`
print(sum(ma_liste))  # Affiche 15

# Fonction intégrée `min()`
print(min(ma_liste))  # Affiche 1

# Fonction intégrée `max()`
print(max(ma_liste))  # Affiche 5

# Fonction intégrée `sorted()`
print(sorted(ma_liste))  # Affiche [1, 2, 3, 4, 5]
```

## Copie d'une liste
Il est possible de copier une liste en Python en utilisant l'opérateur `=`. Cependant, il faut faire attention car la copie d'un objet en Python est une copie par référence. Cela signifie que si vous modifiez un élément de la liste copiée, vous modifiez également l'élément correspondant dans la liste originale.
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Copie de la liste
ma_liste_2 = ma_liste

# Modification d'un élément de la liste
ma_liste_2[1] = 6
print(ma_liste)  # Affiche [1, 6, 3, 4, 5]
```

Dans cet exemple, nous avons déclaré une liste `ma_liste` et nous avons copié cette liste dans une nouvelle liste `ma_liste_2`. Nous avons ensuite modifié le deuxième élément de la liste `ma_liste_2` et nous avons constaté que le deuxième élément de la liste `ma_liste` a également été modifié.

Pour copier une liste en Python sans modifier la liste originale (deep copy), plusieurs solutions existent. La plus simple est d'utiliser la méthode `list()` :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Deep copie de la liste
ma_liste_2 = list(ma_liste) # Python 2 
ma_liste_2 = ma_liste[:] # Python 2 : slicing
ma_liste_2 = ma_liste.copy() # Python 3.3+
ma_liste_2 = [x for x in ma_liste] # Python 3.5+ : list comprehension
ma_liste_2 = [*ma_liste] # Python 3.5+ : unpacking

# Modification d'un élément de la liste
ma_liste_2[1] = 6
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

## Modification d'une liste
Il est possible de modifier les éléments d'une liste en Python. Pour cela, il suffit d'utiliser l'opérateur d'affectation `=` pour assigner une nouvelle valeur à un élément particulier de la liste.

Voici un exemple de modification d'une liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Modification d'un élément de la liste
ma_liste[1] = 6
print(ma_liste)  # Affiche [1, 6, 3, 4, 5]
```

Dans cet exemple, nous avons déclaré une liste `ma_liste` et nous avons modifié son deuxième élément (dont l'index est 1) en lui assignant la valeur 6.

## Concaténation de listes
Il est possible de concaténer deux listes en Python en utilisant l'opérateur `+`. Voici un exemple de concaténation de listes en Python :
```python
# Déclaration des listes
ma_liste_1 = [1, 2, 3]
ma_liste_2 = [4, 5, 6]

# Concaténation des listes
ma_liste_3 = ma_liste_1 + ma_liste_2
print(ma_liste_3)  # Affiche [1, 2, 3, 4, 5, 6]

# Multiplication des listes
ma_liste_4 = ma_liste_1 * 2
print(ma_liste_4)  # Affiche [1, 2, 3, 1, 2, 3]
```

## Méthodes courantes de manipulation de listes
Il existe plusieurs méthodes courantes pour manipuler les listes en Python. Voici quelques exemples :

### `ma_liste.append(x)`
Ajoute un élément `x` à la fin de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Ajout d'un élément à la liste
ma_liste.append(6)
print(ma_liste)  # Affiche [1, 2, 3, 4, 5, 6]
```

### `ma_liste.extend(iterable)`
Ajoute tous les éléments d'un itérable `iterable` à la fin de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Ajout de plusieurs éléments à la liste
ma_liste.extend([6, 7, 8])
print(ma_liste)  # Affiche [1, 2, 3, 4, 5, 6, 7, 8]
```

### `ma_liste.insert(i, x)`
Insère un élément `x` à l'index `i` de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Insertion d'un élément à la liste
ma_liste.insert(2, 6)
print(ma_liste)  # Affiche [1, 2, 6, 3, 4, 5]
```

### `ma_liste.pop(i)`
Supprime l'élément à l'index `i` de la liste et le retourne :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression d'un élément de la liste
ma_liste.pop(2)
print(ma_liste)  # Affiche [1, 2, 4, 5]
```

### `ma_liste.remove(x)`
Supprime l'élément `x` de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression d'un élément de la liste
ma_liste.remove(3)
print(ma_liste)  # Affiche [1, 2, 4, 5]
```

### `ma_liste.clear()`
Supprime tous les éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression de tous les éléments de la liste
ma_liste.clear()
print(ma_liste)  # Affiche []
```

### `ma_liste.index(x)`
Retourne l'index de l'élément `x` dans la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Recherche de l'index d'un élément de la liste
print(ma_liste.index(3))  # Affiche 2
```

### `ma_liste.count(x)`
Retourne le nombre d'occurrences de l'élément `x` dans la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5, 3]

# Recherche du nombre d'occurrences d'un élément de la liste
print(ma_liste.count(3))  # Affiche 2
```

### `ma_liste.sort()`
Trie les éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [5, 2, 3, 4, 1]

# Tri de la liste
ma_liste.sort()
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

### `ma_liste.reverse()`
Inverse l'ordre des éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Inversion de l'ordre des éléments de la liste
ma_liste.reverse()
print(ma_liste)  # Affiche [5, 4, 3, 2, 1]
```

### `ma_liste.copy()`
Retourne une copie de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Copie de la liste
ma_liste_copie = ma_liste.copy()
print(ma_liste_copie)  # Affiche [1, 2, 3, 4, 5]
```

## Boucler sur une liste
Il est possible de boucler sur une liste en Python en utilisant la boucle `for`. Voici un exemple de boucle sur une liste en Python :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Boucle sur la liste
for element in ma_liste:
    print(element)
```
Cet exemple va afficher chaque élément de la liste sur une ligne différente :
```python
1
2
3
4
5
```

Il est important de noter que ces méthodes modifient la liste sur laquelle elles sont appelées. Si vous souhaitez créer une nouvelle liste sans modifier l'originale, vous pouvez utiliser des techniques avancées comme le slicing ou la compréhension de liste (cf. ci-après).

## Utilisation avancée des listes
Les listes en Python offrent de nombreuses possibilités pour manipuler les données de manière efficace. Voici quelques exemples d'utilisations avancées des listes :

### Slicing
Il est possible de créer une nouvelle liste à partir d'une liste existante en utilisant le slicing. Le slicing permet de sélectionner une partie d'une liste en utilisant la syntaxe suivante : `ma_liste[start:stop:step]`. Voici un exemple de slicing sur une liste en Python :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[1:4:1]
print(ma_liste_copie)  # Affiche [2, 3, 4]
```

Le slicing permet de créer une nouvelle liste en sélectionnant une partie de la liste originale. Dans cet exemple, on sélectionne tous les éléments de la liste originale en commençant à l'index 0 et en allant jusqu'à l'index 5 (non inclus) avec un pas de 1. Si vous souhaitez sélectionner tous les éléments de la liste, vous pouvez omettre les paramètres `start` et `stop` :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[:]
print(ma_liste_copie)  # Affiche [1, 2, 3, 4, 5]
```

Le slicing permet également de sélectionner des éléments en partant de la fin de la liste en utilisant des index négatifs. Par exemple, pour sélectionner les 3 derniers éléments de la liste, vous pouvez utiliser le slicing suivant :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[-3:]
print(ma_liste_copie)  # Affiche [3, 4, 5]
```

Le premier élément du slicing peut être omis pour sélectionner tous les éléments jusqu'à l'index `stop` :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[:4]
print(ma_liste_copie)  # Affiche [1, 2, 3, 4]
```

Le slicing permet également de sélectionner des éléments avec un pas différent de 1. Par exemple, pour sélectionner les éléments de la liste avec un pas de 2, vous pouvez utiliser le slicing suivant :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[::2]
print(ma_liste_copie)  # Affiche [1, 3, 5]
```

### Compréhension de liste
Il est possible de créer une nouvelle liste à partir d'une liste existante en utilisant la compréhension de liste. La compréhension de liste permet de créer une nouvelle liste en appliquant une fonction à chaque élément d'une liste. Voici un exemple de compréhension de liste en Python :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = [element * 2 for element in ma_liste]
print(ma_liste_copie)  # Affiche [2, 4, 6, 8, 10]
```

La compréhension de liste permet de créer une nouvelle liste en appliquant une fonction à chaque élément d'une liste. Dans cet exemple, on multiplie chaque élément de la liste originale par 2. La compréhension de liste permet également d'ajouter des conditions à la création de la nouvelle liste. Par exemple, pour créer une nouvelle liste contenant uniquement les éléments pairs de la liste originale, vous pouvez utiliser la compréhension de liste suivante :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = [element for element in ma_liste if element % 2 == 0]
print(ma_liste_copie)  # Affiche [2, 4]
```

### Unpacking
Il est possible de décomposer une liste en utilisant l'unpacking. L'unpacking permet de décomposer une liste en plusieurs variables. Voici un exemple d'unpacking en Python :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Décomposition de la liste
a, b, c, d, e = ma_liste
print(a)  # Affiche 1
print(b)  # Affiche 2
print(c)  # Affiche 3
print(d)  # Affiche 4
print(e)  # Affiche 5
```

L'unpacking permet de décomposer une liste en plusieurs variables. Dans cet exemple, on décompose la liste en 5 variables. Il est important de noter que le nombre de variables doit correspondre au nombre d'éléments de la liste. Si vous souhaitez décomposer une liste en moins de variables, vous pouvez utiliser l'opérateur `*` :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Décomposition de la liste
a, b, *c = ma_liste
print(a)  # Affiche 1
print(b)  # Affiche 2
print(c)  # Affiche [3, 4, 5]

# Décomposition de la liste
*a, b, c = ma_liste
print(a)  # Affiche [1, 2, 3]
print(b)  # Affiche 4
print(c)  # Affiche 5

# Décomposition de la liste
*a, = ma_liste # Notez la virgule après la variable `a` afin d'indiquer un tuple
print(a)  # Affiche [1, 2, 3, 4, 5]

# Décomposition de la liste
ma_liste2 = [*ma_liste]
print(ma_liste2)  # Affiche [1, 2, 3, 4, 5]
```
