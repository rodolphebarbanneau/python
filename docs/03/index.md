---
layout: default
title: Variables avancées
nav_order: 5
---

# Variables avancées

![For loop sucks!](../assets/for_loop_sucks.png)

## Cheatsheet
```python
"""
Les listes (list) :
Utilisation pour des collections ordonnées d'éléments modifiables
"""
ma_liste = [1, 2, 2, 3, 3, 3] # Déclaration d'une liste
ma_liste.append(4) # Ajouter un élément à la fin de la liste [1, 2, 2, 3, 3, 3, 4]
ma_liste[0] = 0 # Modifier un élément de la liste [0, 2, 2, 3, 3, 3, 4]
ma_liste.pop() # Supprimer le dernier élément de la liste [0, 2, 2, 3, 3, 3]
print(ma_liste) # Afficher la liste

# Slicing
ma_liste = ma_liste[1:] # Supprimer le premier élément de la liste [2, 2, 3, 3, 3]
ma_liste = ma_liste[:-1] # Supprimer le dernier élément de la liste [2, 2, 3, 3]
ma_liste = ma_liste[1:-1] # Supprimer le premier et le dernier élément de la liste [2, 3, 3]
ma_liste = ma_liste[::2] # Supprimer tous les éléments d'index pairs de la liste [2, 3]
ma_liste = ma_liste[::-1] # Inverser l'ordre des éléments de la liste [3, 2]
print(ma_liste) # Afficher la liste

# Compréhension de liste
ma_liste = [x for x in range(10)] # Créer une liste de 10 éléments de 0 à 9
ma_liste = [x for x in range(10) if x % 2 == 0] # Créer une liste de 5 éléments pairs de 0 à 8
print(ma_liste) # Afficher la liste [0, 2, 4, 6, 8]

"""
Les tuples (tuple) :
Utilisation pour des collections ordonnées d'éléments immuables
"""
mon_tuple = (1, 2, 2, 3) # Déclaration d'un tuple
a, b, c, d = mon_tuple # Déballage d'un tuple
mon_tuple[0] # Accès à un élément d'un tuple
mon_tuple[0] = 0 # Erreur : un tuple est immuable
print(a, b, c, d) # Afficher les éléments du tuple (1, 2, 2, 3)

"""
Les ensembles (set) :
Utilisation pour des collections non-ordonnées d'éléments uniques
"""
mon_set = {1, 2, 3} # Déclaration d'un ensemble
mon_set.add(4) # Ajouter un élément à l'ensemble
mon_set.add(4) # Ajouter un élément déjà présent à l'ensemble
mon_set.discard(3) # Supprimer un élément de l'ensemble
print(mon_set) # Afficher l'ensemble {1, 2, 4}

"""
Les dictionnaires (dict) :
Utilisation pour des collections non-ordonnées de paires clé-valeur
"""
mon_dict = {"cle1": "valeur1", "cle2": "valeur2"} # Déclaration d'un dictionnaire
mon_dict["cle1"] # Accès à une valeur via sa clé
mon_dict["cle3"] = "valeur3" # Ajout d'une paire clé-valeur
del mon_dict["cle2"] # Suppression d'une paire clé-valeur
print(mon_dict) # Afficher le dictionnaire {"cle1": "valeur1", "cle3": "valeur3"}
```

## Partie 1 : Les listes

### Qu'est-ce qu'une liste en Python ?
En Python, une liste est une collection ordonnée d'éléments, pouvant être de différents types (nombres, chaînes de caractères, booléens, autres listes, etc.). Les éléments d'une liste sont séparés par des virgules et encadrés par des crochets `[ ]`.

### Création d'une liste en Python
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

### Accès aux éléments d'une liste en Python
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

### Fonctions intégrées en Python pour manipuler les listes
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

### Modification d'une liste en Python
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

### Concaténation de listes en Python
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

### Méthodes courantes de manipulation de listes en Python
Il existe plusieurs méthodes courantes pour manipuler les listes en Python. Voici quelques exemples :

#### `ma_liste.append(x)`
Ajoute un élément `x` à la fin de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Ajout d'un élément à la liste
ma_liste.append(6)
print(ma_liste)  # Affiche [1, 2, 3, 4, 5, 6]
```

#### `ma_liste.extend(iterable)`
Ajoute tous les éléments d'un itérable `iterable` à la fin de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Ajout de plusieurs éléments à la liste
ma_liste.extend([6, 7, 8])
print(ma_liste)  # Affiche [1, 2, 3, 4, 5, 6, 7, 8]
```

#### `ma_liste.insert(i, x)`
Insère un élément `x` à l'index `i` de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Insertion d'un élément à la liste
ma_liste.insert(2, 6)
print(ma_liste)  # Affiche [1, 2, 6, 3, 4, 5]
```

#### `ma_liste.pop(i)`
Supprime l'élément à l'index `i` de la liste et le retourne :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression d'un élément de la liste
ma_liste.pop(2)
print(ma_liste)  # Affiche [1, 2, 4, 5]
```

#### `ma_liste.remove(x)`
Supprime l'élément `x` de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression d'un élément de la liste
ma_liste.remove(3)
print(ma_liste)  # Affiche [1, 2, 4, 5]
```

#### `ma_liste.clear()`
Supprime tous les éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Suppression de tous les éléments de la liste
ma_liste.clear()
print(ma_liste)  # Affiche []
```

#### `ma_liste.index(x)`
Retourne l'index de l'élément `x` dans la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Recherche de l'index d'un élément de la liste
print(ma_liste.index(3))  # Affiche 2
```

#### `ma_liste.count(x)`
Retourne le nombre d'occurrences de l'élément `x` dans la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5, 3]

# Recherche du nombre d'occurrences d'un élément de la liste
print(ma_liste.count(3))  # Affiche 2
```

#### `ma_liste.sort()`
Trie les éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [5, 2, 3, 4, 1]

# Tri de la liste
ma_liste.sort()
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

#### `ma_liste.reverse()`
Inverse l'ordre des éléments de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Inversion de l'ordre des éléments de la liste
ma_liste.reverse()
print(ma_liste)  # Affiche [5, 4, 3, 2, 1]
```

#### `ma_liste.copy()`
Retourne une copie de la liste :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Copie de la liste
ma_liste_copie = ma_liste.copy()
print(ma_liste_copie)  # Affiche [1, 2, 3, 4, 5]
```

### Boucler sur une liste en Python
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

### Utilisation avancée des listes en Python
Les listes en Python offrent de nombreuses possibilités pour manipuler les données de manière efficace. Voici quelques exemples d'utilisations avancées des listes :

#### Slicing
Il est possible de créer une nouvelle liste à partir d'une liste existante en utilisant le slicing. Le slicing permet de sélectionner une partie d'une liste en utilisant la syntaxe suivante : `ma_liste[start:stop:step]`. Voici un exemple de slicing sur une liste en Python :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[0:5:1]
print(ma_liste_copie)  # Affiche [1, 2, 3, 4, 5]
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
Le slicing permet également de sélectionner des éléments avec un pas différent de 1. Par exemple, pour sélectionner les éléments de la liste avec un pas de 2, vous pouvez utiliser le slicing suivant :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5]

# Création d'une nouvelle liste à partir de la liste originale
ma_liste_copie = ma_liste[::2]
print(ma_liste_copie)  # Affiche [1, 3, 5]
```

#### Compréhension de liste
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

## Partie 2 : Les tuples
Les tuples sont des structures de données similaires aux listes, mais qui ont quelques différences importantes. Les tuples sont immuables, ce qui signifie qu'ils ne peuvent pas être modifiés après leur création. En outre, les tuples peuvent être utilisés comme clés dans les dictionnaires, ce qui n'est pas possible avec les listes.

### Création de tuples
Les tuples sont créés en utilisant des parenthèses plutôt que des crochets. Voici un exemple :
```python
# Déclaration du tuple
mon_tuple = (1, 2, 3)

# Modification du tuple
mon_tuple[0] = 6  # Erreur
```

Il est également possible de créer un tuple avec une seule valeur en ajoutant une virgule à la fin :
```python
# Déclaration du tuple
mon_tuple = (1,)
```

### Accès aux éléments des tuples
Les éléments des tuples sont accessibles de la même manière que pour les listes, en utilisant des index. Par exemple :
```python
mon_tuple = (1, 2, 3)
print(mon_tuple[0]) # affiche 1
print(mon_tuple[1]) # affiche 2
print(mon_tuple[2]) # affiche 3
```

Il n'est cependant pas possible de modifier les éléments d'un tuple après sa création.

### Utilisations avancées des tuples
Les tuples sont souvent utilisés dans des fonctions pour renvoyer plusieurs valeurs. Voici un exemple :
```python
def divmod(a, b):
    quotient = a // b
    reste = a % b
    return quotient, reste

resultat = divmod(10, 3)
print(resultat) # affiche (3, 1)
```

Dans cet exemple, la fonction divmod renvoie deux valeurs en utilisant un tuple. La variable resultat contient ensuite ce tuple.

En conclusion, les tuples sont utiles dans des situations où l'on veut des données immuables et où l'on veut pouvoir utiliser des objets comme des clés dans des dictionnaires. Bien qu'ils ne soient pas aussi flexibles que les listes, ils sont néanmoins très utiles dans certaines situations.

## Partie 3 : Les ensembles
En Python, les ensembles (ou sets) sont des collections de données non ordonnées et non indexées. Les ensembles sont représentés par des accolades ({}) et peuvent contenir différents types de données, comme des entiers, des chaînes de caractères ou encore des tuples.

Les ensembles ont plusieurs avantages :
- Ils permettent de stocker une collection d'éléments uniques. Cela signifie qu'il n'y aura pas de doublons dans un ensemble.
- Les ensembles offrent des opérations mathématiques comme l'union, l'intersection et la différence qui peuvent être très utiles pour travailler avec des ensembles de données.

### Création d'un ensemble
Pour créer un ensemble en Python, on utilise la fonction `set()` ou on peut également déclarer un ensemble vide avec des accolades `{}`. Par exemple :
```python
# Création d'un ensemble à partir d'une liste
mon_ensemble = set([1, 2, 3, 4, 5])
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5}

# Création d'un ensemble vide
mon_ensemble = set()
print(type(mon_ensemble))  # Affiche <class 'set'>
```

On peut également créer un ensemble directement avec des accolades, comme ceci :
```python
# Création d'un ensemble
mon_ensemble = {1, 2, 3, 4, 5}
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5}

# Création d'un ensemble vide
mon_ensemble = {}
print(type(mon_ensemble))  # Affiche <class 'dict'>
```

Les éléments d'un ensemble ne sont pas indexés, donc il n'est pas possible d'accéder à un élément en utilisant un index. Par exemple :
```python
mon_ensemble = {1, 2, 3, 4, 5}
print(mon_ensemble[0])  # Erreur
```

### Accès aux éléments d'un ensemble
Il n'est pas possible d'accéder aux éléments d'un ensemble en utilisant un index. Cependant, il est possible de vérifier si un élément est présent dans un ensemble en utilisant l'opérateur `in`. Par exemple :
```python
mon_ensemble = {1, 2, 3, 4, 5}
print(1 in mon_ensemble)  # Affiche True
print(6 in mon_ensemble)  # Affiche False
```

### Fonctions intégrées en Python pour manipuler les ensembles
Il existe de nombreuses fonctions intégrées en Python qui permettent de manipuler les ensembles, notamment :
- **`len(mon_ensemble)`** : renvoie le nombre d'éléments de l'ensemble `mon_ensemble`.
- **`max(mon_ensemble)`** : renvoie l'élément le plus grand de l'ensemble `mon_ensemble`.
- **`min(mon_ensemble)`** : renvoie l'élément le plus petit de l'ensemble `mon_ensemble`.
- **`sorted(mon_ensemble)`** : renvoie une liste triée des éléments de l'ensemble `mon_ensemble`.
- **`sum(mon_ensemble)`** : renvoie la somme des éléments de l'ensemble `mon_ensemble`.
- **`any(mon_ensemble)`** : renvoie True si au moins un élément de l'ensemble `mon_ensemble` est vrai.
- **`all(mon_ensemble)`** : renvoie True si tous les éléments de l'ensemble `mon_ensemble` sont vrais.
- **`enumerate(mon_ensemble)`** : renvoie un objet enumerate qui peut être utilisé pour parcourir l'ensemble `mon_ensemble`.
- **`zip(mon_ensemble)`** : renvoie un objet zip qui peut être utilisé pour parcourir plusieurs ensembles en même temps.

### Opérations mathématiques sur les ensembles
Les ensembles ont plusieurs opérations mathématiques qui peuvent être très utiles pour travailler avec des ensembles de données. Voici quelques exemples :
```python
# Création de deux ensembles
ensemble1 = {1, 2, 3, 4, 5}
ensemble2 = {4, 5, 6, 7, 8}

# Union
ensemble3 = ensemble1 | ensemble2
print(ensemble3)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}

# Intersection
ensemble3 = ensemble1 & ensemble2
print(ensemble3)  # Affiche {4, 5}

# Différence
ensemble3 = ensemble1 - ensemble2
print(ensemble3)  # Affiche {1, 2, 3}

# Différence symétrique
ensemble3 = ensemble1 ^ ensemble2
print(ensemble3)  # Affiche {1, 2, 3, 6, 7, 8}

# Sous-ensemble
print({1, 2, 3} <= ensemble1)  # Affiche True
print({1, 2, 3} <= ensemble2)  # Affiche False

# Super-ensemble
print(ensemble1 >= {1, 2, 3})  # Affiche True
print(ensemble2 >= {1, 2, 3})  # Affiche False

# Égalité
print({1, 2, 3} == {3, 2, 1})  # Affiche True
print({1, 2, 3} == {1, 2, 3, 4})  # Affiche False

# Inégalité
print({1, 2, 3} != {3, 2, 1})  # Affiche False
print({1, 2, 3} != {1, 2, 3, 4})  # Affiche True

# Égalité stricte
print({1, 2, 3} is {3, 2, 1})  # Affiche False
print({1, 2, 3} is {1, 2, 3})  # Affiche False

# Inégalité stricte
print({1, 2, 3} is not {3, 2, 1})  # Affiche True
print({1, 2, 3} is not {1, 2, 3})  # Affiche True

# Inclusion
print({1, 2, 3} < {1, 2, 3, 4})  # Affiche True
print({1, 2, 3} < {1, 2, 3})  # Affiche False

# Non-inclusion
print({1, 2, 3} > {1, 2, 3, 4})  # Affiche False
print({1, 2, 3} > {1, 2, 3})  # Affiche False
```

### Méthodes courantes de manipulation d'ensembles en Python
Il existe plusieurs méthodes courantes pour manipuler les ensembles en Python. Voici quelques exemples :

#### `mon_ensemble.add(x)`
Ajoute un élément `x` à l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Ajout d'un élément à l'ensemble
mon_ensemble.add(6)
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5, 6}
```

#### `mon_ensemble.clear()`
Supprime tous les éléments de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de tous les éléments de l'ensemble
mon_ensemble.clear()
print(mon_ensemble)  # Affiche set()
```

#### `mon_ensemble.copy()`
Renvoie une copie de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Copie de l'ensemble
mon_ensemble2 = mon_ensemble.copy()
print(mon_ensemble2)  # Affiche {1, 2, 3, 4, 5}
```

#### `mon_ensemble.difference(mon_ensemble2)`
Renvoie la différence entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Différence entre les deux ensembles
mon_ensemble3 = mon_ensemble.difference(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3}
```

#### `mon_ensemble.difference_update(mon_ensemble2)`
Supprime tous les éléments de l'ensemble qui sont également présents dans l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments communs entre les deux ensembles
mon_ensemble.difference_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3}
```

#### `mon_ensemble.discard(x)`
Supprime l'élément `x` de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de l'élément 3 de l'ensemble
mon_ensemble.discard(3)
print(mon_ensemble)  # Affiche {1, 2, 4, 5}
```

#### `mon_ensemble.intersection(mon_ensemble2)`
Renvoie l'intersection entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Intersection entre les deux ensembles
mon_ensemble3 = mon_ensemble.intersection(mon_ensemble2)
print(mon_ensemble3)  # Affiche {4, 5}
```

#### `mon_ensemble.intersection_update(mon_ensemble2)`
Supprime tous les éléments de l'ensemble qui ne sont pas présents dans l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments qui ne sont pas communs entre les deux ensembles
mon_ensemble.intersection_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {4, 5}
```

#### `mon_ensemble.isdisjoint(mon_ensemble2)`
Renvoie `True` si l'ensemble et l'ensemble `mon_ensemble2` ne possèdent aucun élément commun, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'intersection entre les deux ensembles
print(mon_ensemble.isdisjoint(mon_ensemble2))  # Affiche False
```

#### `mon_ensemble.issubset(mon_ensemble2)`
Renvoie `True` si l'ensemble est inclus dans l'ensemble `mon_ensemble2`, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'inclusion entre les deux ensembles
print(mon_ensemble.issubset(mon_ensemble2))  # Affiche False
```

#### `mon_ensemble.issuperset(mon_ensemble2)`
Renvoie `True` si l'ensemble est inclus dans l'ensemble `mon_ensemble2`, `False` sinon :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Vérification de l'inclusion entre les deux ensembles
print(mon_ensemble.issuperset(mon_ensemble2))  # Affiche False
```

#### `mon_ensemble.pop()`
Supprime un élément au hasard de l'ensemble et le renvoie :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression d'un élément au hasard de l'ensemble
mon_ensemble.pop()
print(mon_ensemble)  # Affiche {2, 3, 4, 5}
```

#### `mon_ensemble.remove(x)`
Supprime l'élément `x` de l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Suppression de l'élément 3 de l'ensemble
mon_ensemble.remove(3)
print(mon_ensemble)  # Affiche {1, 2, 4, 5}
```

#### `mon_ensemble.symmetric_difference(mon_ensemble2)`
Renvoie la différence symétrique entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Différence symétrique entre les deux ensembles
mon_ensemble3 = mon_ensemble.symmetric_difference(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3, 6, 7, 8}
```

#### `mon_ensemble.symmetric_difference_update(mon_ensemble2)`

Supprime tous les éléments de l'ensemble qui sont également présents dans l'ensemble `mon_ensemble2` et ajoute tous les éléments de l'ensemble `mon_ensemble2` qui ne sont pas présents dans l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Suppression des éléments communs entre les deux ensembles
mon_ensemble.symmetric_difference_update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3, 6, 7, 8}
```

#### `mon_ensemble.union(mon_ensemble2)`
Renvoie l'union entre l'ensemble et l'ensemble `mon_ensemble2` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Union entre les deux ensembles
mon_ensemble3 = mon_ensemble.union(mon_ensemble2)
print(mon_ensemble3)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}
```

#### `mon_ensemble.update(mon_ensemble2)`
Ajoute tous les éléments de l'ensemble `mon_ensemble2` à l'ensemble :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Déclaration d'un autre ensemble
mon_ensemble2 = {4, 5, 6, 7, 8}

# Ajout des éléments de l'ensemble 2 à l'ensemble 1
mon_ensemble.update(mon_ensemble2)
print(mon_ensemble)  # Affiche {1, 2, 3, 4, 5, 6, 7, 8}
```

### Boucler sur un ensemble en Python
Il est possible de boucler sur un ensemble en Python grâce à la boucle `for` :
```python
# Déclaration de l'ensemble
mon_ensemble = {1, 2, 3, 4, 5}

# Boucle sur l'ensemble
for element in mon_ensemble:
    print(element)
```

### Utilisation avancée des ensembles en Python
Les ensembles en Python peuvent être utilisés pour effectuer des opérations sur des listes ou des chaînes de caractères.

#### Suppression des doublons d'une liste
Il est possible de supprimer les doublons d'une liste en utilisant un ensemble :
```python
# Déclaration de la liste
ma_liste = [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]

# Suppression des doublons de la liste
ma_liste = list(set(ma_liste))
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

#### Suppression des doublons d'une chaîne de caractères
Il est possible de supprimer les doublons d'une chaîne de caractères en utilisant un ensemble :
```python
# Déclaration de la chaîne de caractères
ma_chaine = "Hello World"

# Suppression des doublons de la chaîne de caractères
ma_chaine = "".join(set(ma_chaine))
print(ma_chaine)  # Affiche "Helo Wrd"
```

#### Comptage des caractères d'une chaîne de caractères
Il est possible de compter les caractères d'une chaîne de caractères en utilisant un ensemble :
```python
# Déclaration de la chaîne de caractères
ma_chaine = "Hello World"

# Comptage des caractères de la chaîne de caractères
mon_ensemble = set(ma_chaine)
print(len(mon_ensemble))  # Affiche 8
```

## Partie 4 : Les dictionnaires
Un dictionnaire est une structure de données qui permet de stocker des paires de clés-valeurs. En Python, un dictionnaire est défini avec des accolades `{}` et les paires clé-valeur sont séparées par des virgules `,`. La clé et la valeur sont séparées par un deux-points `:`.

### Création d'un dictionnaire en Python
Pour déclarer un dictionnaire avec des paires clé-valeur en Python, il suffit d'utiliser des accolades `{}` et de séparer les paires clé-valeur par des virgules `,` :
```python
# Déclaration d'un dictionnaire vide
mon_dictionnaire = {}

# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}
```

### Accès aux valeurs d'un dictionnaire en Python
Pour accéder à une valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Accès à la valeur de la clé "nom"
print(mon_dictionnaire["nom"])  # Affiche "Dupont"
```

### Modification des valeurs d'un dictionnaire en Python
Pour modifier une valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Modification de la valeur de la clé "nom"
mon_dictionnaire["nom"] = "Durand"
print(mon_dictionnaire)  # Affiche {"nom": "Durand", "prenom": "Jean", "age": 25}
```

### Ajout de paires clé-valeur dans un dictionnaire en Python
Pour ajouter une paire clé-valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Ajout d'une paire clé-valeur
mon_dictionnaire["ville"] = "Paris"
print(mon_dictionnaire)  # Affiche {"nom": "Dupont", "prenom": "Jean", "age": 25, "ville": "Paris"}
```

### Suppression d'une paire clé-valeur dans un dictionnaire en Python
Pour supprimer une paire clé-valeur dans un dictionnaire, vous pouvez utiliser la méthode `pop()` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression de la paire clé-valeur (méthode pop)
mon_dictionnaire.pop("nom")
print(mon_dictionnaire)  # Affiche {"prenom": "Jean", "age": 25}

# Suppression de la paire clé-valeur (méthode del)
del mon_dictionnaire["prenom"]
print(mon_dictionnaire)  # Affiche {"age": 25}
```

### Parcours des paires clé-valeur d'un dictionnaire en Python
Il est possible de parcourir les paires clé-valeur d'un dictionnaire en Python grâce à la boucle `for`, la méthode `items()` est utilisée pour parcourir simultanément les clés et les valeurs du dictionnaire
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Parcours des paires clé-valeur (méthode sans tuple)
for cle in mon_dictionnaire:
    print(cle, mon_dictionnaire[cle])

# Parcours des paires clé-valeur (méthode avec tuple)
for cle, valeur in mon_dictionnaire.items():
    print(cle, valeur)
```

### Concaténation de dictionnairs en Python
Il est possible de concaténer deux dictionnaires en Python en utilisant l'opérateur `+`. Voici un exemple de concaténation de dictionnaires en Python :
```python
# Déclaration des dictionnaires
mon_dictionnaire_1 = {"nom": "Dupont", "prenom": "Jean", "age": 25}
mon_dictionnaire_2 = {"ville": "Paris", "pays": "France"}

# Concaténation des dictionnaires
mon_dictionnaire_3 = mon_dictionnaire_1 + mon_dictionnaire_2
print(mon_dictionnaire_3)  # Affiche {"nom": "Dupont", "prenom": "Jean", "age": 25, "ville": "Paris", "pays": "France"}
```

### Fonctions intégrées en Python pour manipuler les dictionnaires
Il existe plusieurs fonctions intégrées en Python qui permettent de manipuler les dictionnaires, notamment :
- **`dict(mon_iterable)`** : permet de créer un dictionnaire à partir d'un itérable `mon_iterable` (comme un tuple).
- **`len(mon_dictionnaire)`** : renvoie le nombre de paires clé-valeur du dictionnaire `mon_dictionnaire`.

### Méthodes courantes de manipulation de dictionnaires en Python
Python propose de nombreuses méthodes pour manipuler les dictionnaires.

#### `mon_dictionnaire.keys()`
Renvoie la liste des clés du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des clés du dictionnaire
print(mon_dictionnaire.keys())  # Affiche dict_keys(['nom', 'prenom', 'age'])
```

#### `mon_dictionnaire.values()`
Renvoie la liste des valeurs du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des valeurs du dictionnaire
print(mon_dictionnaire.values())  # Affiche dict_values(['Dupont', 'Jean', 25])
```

#### `mon_dictionnaire.items()`
Renvoie la liste des paires clé-valeur du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des paires clé-valeur du dictionnaire
print(mon_dictionnaire.items())  # Affiche dict_items([('nom', 'Dupont'), ('prenom', 'Jean'), ('age', 25)])
```

#### `mon_dictionnaire.get(cle, valeur_par_defaut)`
Renvoie la valeur associée à la clé `cle` du dictionnaire `mon_dictionnaire`, si la clé n'existe pas, renvoie la valeur `valeur_par_defaut` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération de la valeur associée à la clé "nom"
print(mon_dictionnaire.get("nom"))  # Affiche "Dupont"

# Récupération de la valeur associée à la clé "ville"
print(mon_dictionnaire.get("ville"))  # Affiche None

# Récupération de la valeur associée à la clé "ville" avec une valeur par défaut
print(mon_dictionnaire.get("ville", "Paris"))  # Affiche "Paris"
```

#### `mon_dictionnaire.pop(cle)`
Supprime la paire clé-valeur associée à la clé `cle` du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression de la paire clé-valeur associée à la clé "nom"
mon_dictionnaire.pop("nom")
print(mon_dictionnaire)  # Affiche {'prenom': 'Jean', 'age': 25}
```

#### `mon_dictionnaire.popitem()`
Supprime une paire clé-valeur au hasard du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression d'une paire clé-valeur au hasard
mon_dictionnaire.popitem()
print(mon_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean'}
```

#### `mon_dictionnaire.clear()`
Supprime toutes les paires clé-valeur du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression de toutes les paires clé-valeur
mon_dictionnaire.clear()
print(mon_dictionnaire)  # Affiche {}
```

#### `mon_dictionnaire.update(mon_autre_dictionnaire)`
Ajoute les paires clé-valeur du dictionnaire `mon_autre_dictionnaire` au dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Déclaration d'un autre dictionnaire
mon_autre_dictionnaire = {"ville": "Paris", "pays": "France"}

# Ajout des paires clé-valeur du dictionnaire "mon_autre_dictionnaire" au dictionnaire "mon_dictionnaire"
mon_dictionnaire.update(mon_autre_dictionnaire)
print(mon_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean', 'age': 25, 'ville': 'Paris', 'pays': 'France'}
```

#### `mon_dictionnaire.copy()`
Renvoie une copie du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Copie du dictionnaire
mon_autre_dictionnaire = mon_dictionnaire.copy()
print(mon_autre_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean', 'age': 25}
```

#### `mon_dictionnaire.setdefault(cle, valeur_par_defaut)`
Renvoie la valeur associée à la clé `cle` du dictionnaire `mon_dictionnaire`, si la clé n'existe pas, ajoute la paire clé-valeur `cle`-`valeur_par_defaut` au dictionnaire et renvoie la valeur `valeur_par_defaut` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération de la valeur associée à la clé "nom"
print(mon_dictionnaire.setdefault("nom"))  # Affiche "Dupont"

# Récupération de la valeur associée à la clé "ville"
print(mon_dictionnaire.setdefault("ville"))  # Affiche None

# Récupération de la valeur associée à la clé "ville" avec une valeur par défaut
print(mon_dictionnaire.setdefault("ville", "Paris"))  # Affiche "Paris"

# Affichage du dictionnaire
print(mon_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean', 'age': 25, 'ville': 'Paris'}
```

#### `mon_dictionnaire.fromkeys(liste_cles, valeur_par_defaut)`
Crée un dictionnaire avec les clés de la liste `liste_cles` et la valeur `valeur_par_defaut` :
```python
# Déclaration de la liste
liste_cles = ["nom", "prenom", "age"]

# Création du dictionnaire
mon_dictionnaire = dict.fromkeys(liste_cles, "inconnu")
print(mon_dictionnaire)  # Affiche {'nom': 'inconnu', 'prenom': 'inconnu', 'age': 'inconnu'}
```

### Utilisation avancée des dictionnaires en Python
Python permet d'utiliser des dictionnaires de manière avancée. Nous allons voir comment utiliser des dictionnaires comme des objets, comment utiliser des dictionnaires comme des tableaux associatifs, comment utiliser des dictionnaires comme des tableaux à deux dimensions et comment utiliser des dictionnaires comme des tableaux à plusieurs dimensions.

#### Utilisation des dictionnaires comme des objets
Les dictionnaires peuvent être utilisés comme des objets. Pour cela, il suffit de déclarer un dictionnaire avec des clés qui correspondent aux noms des attributs de l'objet et des valeurs qui correspondent aux valeurs des attributs de l'objet :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Affichage des attributs de l'objet
print(mon_dictionnaire["nom"])  # Affiche "Dupont"
print(mon_dictionnaire["prenom"])  # Affiche "Jean"
print(mon_dictionnaire["age"])  # Affiche 25
```

#### Utilisation des dictionnaires comme des tableaux associatifs
Les dictionnaires peuvent être utilisés comme des tableaux associatifs. Pour cela, il suffit de déclarer un dictionnaire avec des clés qui correspondent aux indices des éléments du tableau associatif et des valeurs qui correspondent aux valeurs des éléments du tableau associatif :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"0": "Dupont", "1": "Jean", "2": 25}

# Affichage des éléments du tableau associatif
print(mon_dictionnaire["0"])  # Affiche "Dupont"
print(mon_dictionnaire["1"])  # Affiche "Jean"
print(mon_dictionnaire["2"])  # Affiche 25
```

#### Utilisation des dictionnaires comme des tableaux à deux dimensions
Les dictionnaires peuvent être utilisés comme des tableaux à deux dimensions. Pour cela, il suffit de déclarer un dictionnaire avec des clés qui correspondent aux indices des lignes du tableau à deux dimensions et des valeurs qui correspondent aux lignes du tableau à deux dimensions :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"0": ["Dupont", "Jean", 25], "1": ["Durand", "Paul", 30]}

# Affichage des éléments du tableau à deux dimensions
print(mon_dictionnaire["0"][0])  # Affiche "Dupont"
print(mon_dictionnaire["0"][1])  # Affiche "Jean"
print(mon_dictionnaire["0"][2])  # Affiche 25
print(mon_dictionnaire["1"][0])  # Affiche "Durand"
print(mon_dictionnaire["1"][1])  # Affiche "Paul"
print(mon_dictionnaire["1"][2])  # Affiche 30
```

## Partie 5 : Exercices

### Exercice 1 : Tri d'une liste
> Écrire un programme Python qui demande à l'utilisateur de saisir une liste de nombres entiers. Le programme doit trier cette liste en ordre croissant et afficher le résultat.

[Solution](./exercices/01.py)

### Exercice 2 : Fusion de dictionnaires
> Écrire une fonction Python qui prend en entrée deux dictionnaires et qui retourne un nouveau dictionnaire contenant les clés et les valeurs de chaque dictionnaire. Si une clé existe dans les deux dictionnaires, la valeur correspondante doit être la somme des valeurs correspondantes.

>Par exemple, si le premier dictionnaire est `{'a': 1, 'b': 2}` et le deuxième dictionnaire est `{'b': 3, 'c': 4}`, le dictionnaire résultant devrait être `{'a': 1, 'b': 5, 'c': 4}`.

[Solution](./exercices/02.py)

### Exercice 3 : Recherche d'éléments dans un ensemble
> Écrire un programme Python qui définit un ensemble d'éléments (par exemple, des noms de fruits) et demande à l'utilisateur de saisir un élément. Le programme doit vérifier si l'élément est présent dans l'ensemble et afficher un message approprié. Ensuite, le programme doit demander à l'utilisateur s'il souhaite ajouter l'élément à l'ensemble et le faire si tel est le cas. Enfin, le programme doit afficher l'ensemble mis à jour.

[Solution](./exercices/03.py)
