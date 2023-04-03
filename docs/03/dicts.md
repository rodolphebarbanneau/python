---
layout: default
title: Dictionnaires `dict`
parent: Variables avancées
nav_order: 4
permalink: /docs/variables-advanced/dicts
---

# Les dictionnaires
{: .no_toc }
Un dictionnaire est une structure de données qui permet de stocker des paires de clés-valeurs. En Python, un dictionnaire est défini avec des accolades `{}` et les paires clé-valeur sont séparées par des virgules `,`. La clé et la valeur sont séparées par un deux-points `:`.

Les ensembles ont plusieurs avantages :
- Ils permettent de stocker une collection d'éléments uniques. Cela signifie qu'il n'y aura pas de doublons dans un ensemble.
- Les ensembles offrent des opérations mathématiques comme l'union, l'intersection et la différence qui peuvent être très utiles pour travailler avec des ensembles de données.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Création d'un dictionnaire
Pour déclarer un dictionnaire avec des paires clé-valeur en Python, il suffit d'utiliser des accolades `{}` et de séparer les paires clé-valeur par des virgules `,` :
```python
# Déclaration d'un dictionnaire vide
mon_dictionnaire = {}

# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}
```

## Accès aux valeurs d'un dictionnaire
Pour accéder à une valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Accès à la valeur de la clé "nom"
print(mon_dictionnaire["nom"])  # Affiche "Dupont"
```

## Modification des valeurs d'un dictionnaire
Pour modifier une valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Modification de la valeur de la clé "nom"
mon_dictionnaire["nom"] = "Durand"
print(mon_dictionnaire)  # Affiche {"nom": "Durand", "prenom": "Jean", "age": 25}
```

## Ajout de paires clé-valeur dans un dictionnaire
Pour ajouter une paire clé-valeur dans un dictionnaire, vous pouvez utiliser la clé correspondante entre crochets `[]` :
```python
# Déclaration d'un dictionnaire avec des paires clé-valeur
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Ajout d'une paire clé-valeur
mon_dictionnaire["ville"] = "Paris"
print(mon_dictionnaire)  # Affiche {"nom": "Dupont", "prenom": "Jean", "age": 25, "ville": "Paris"}
```

## Suppression d'une paire clé-valeur dans un dictionnaire
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

## Parcours des paires clé-valeur d'un dictionnaire
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

## Concaténation de dictionnairs
Il est possible de concaténer deux dictionnaires en Python en utilisant l'opérateur `+`. Voici un exemple de concaténation de dictionnaires en Python :
```python
# Déclaration des dictionnaires
mon_dictionnaire_1 = {"nom": "Dupont", "prenom": "Jean", "age": 25}
mon_dictionnaire_2 = {"ville": "Paris", "pays": "France"}

# Concaténation des dictionnaires
mon_dictionnaire_3 = mon_dictionnaire_1 + mon_dictionnaire_2
print(mon_dictionnaire_3)  # Affiche {"nom": "Dupont", "prenom": "Jean", "age": 25, "ville": "Paris", "pays": "France"}
```

## Fonctions intégrées pour manipuler les dictionnaires
Il existe plusieurs fonctions intégrées en Python qui permettent de manipuler les dictionnaires, notamment :
- **`dict(mon_iterable)`** : permet de créer un dictionnaire à partir d'un itérable `mon_iterable` (comme un tuple).
- **`len(mon_dictionnaire)`** : renvoie le nombre de paires clé-valeur du dictionnaire `mon_dictionnaire`.

## Méthodes courantes de manipulation de dictionnaires
Python propose de nombreuses méthodes pour manipuler les dictionnaires.

### `mon_dictionnaire.keys()`
Renvoie la liste des clés du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des clés du dictionnaire
print(mon_dictionnaire.keys())  # Affiche dict_keys(['nom', 'prenom', 'age'])
```

### `mon_dictionnaire.values()`
Renvoie la liste des valeurs du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des valeurs du dictionnaire
print(mon_dictionnaire.values())  # Affiche dict_values(['Dupont', 'Jean', 25])
```

### `mon_dictionnaire.items()`
Renvoie la liste des paires clé-valeur du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Récupération des paires clé-valeur du dictionnaire
print(mon_dictionnaire.items())  # Affiche dict_items([('nom', 'Dupont'), ('prenom', 'Jean'), ('age', 25)])
```

### `mon_dictionnaire.get(cle, valeur_par_defaut)`
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

### `mon_dictionnaire.pop(cle)`
Supprime la paire clé-valeur associée à la clé `cle` du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression de la paire clé-valeur associée à la clé "nom"
mon_dictionnaire.pop("nom")
print(mon_dictionnaire)  # Affiche {'prenom': 'Jean', 'age': 25}
```

### `mon_dictionnaire.popitem()`
Supprime une paire clé-valeur au hasard du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression d'une paire clé-valeur au hasard
mon_dictionnaire.popitem()
print(mon_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean'}
```

### `mon_dictionnaire.clear()`
Supprime toutes les paires clé-valeur du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Suppression de toutes les paires clé-valeur
mon_dictionnaire.clear()
print(mon_dictionnaire)  # Affiche {}
```

### `mon_dictionnaire.update(mon_autre_dictionnaire)`
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

### `mon_dictionnaire.copy()`
Renvoie une copie du dictionnaire `mon_dictionnaire` :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Copie du dictionnaire
mon_autre_dictionnaire = mon_dictionnaire.copy()
print(mon_autre_dictionnaire)  # Affiche {'nom': 'Dupont', 'prenom': 'Jean', 'age': 25}
```

### `mon_dictionnaire.setdefault(cle, valeur_par_defaut)`
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

### `mon_dictionnaire.fromkeys(liste_cles, valeur_par_defaut)`
Crée un dictionnaire avec les clés de la liste `liste_cles` et la valeur `valeur_par_defaut` :
```python
# Déclaration de la liste
liste_cles = ["nom", "prenom", "age"]

# Création du dictionnaire
mon_dictionnaire = dict.fromkeys(liste_cles, "inconnu")
print(mon_dictionnaire)  # Affiche {'nom': 'inconnu', 'prenom': 'inconnu', 'age': 'inconnu'}
```

## Utilisation avancée des dictionnaires
Python permet d'utiliser des dictionnaires de manière avancée. Nous allons voir comment utiliser des dictionnaires comme des objets, comment utiliser des dictionnaires comme des tableaux associatifs, comment utiliser des dictionnaires comme des tableaux à deux dimensions et comment utiliser des dictionnaires comme des tableaux à plusieurs dimensions.

### Utilisation des dictionnaires comme des objets
Les dictionnaires peuvent être utilisés comme des objets. Pour cela, il suffit de déclarer un dictionnaire avec des clés qui correspondent aux noms des attributs de l'objet et des valeurs qui correspondent aux valeurs des attributs de l'objet :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"nom": "Dupont", "prenom": "Jean", "age": 25}

# Affichage des attributs de l'objet
print(mon_dictionnaire["nom"])  # Affiche "Dupont"
print(mon_dictionnaire["prenom"])  # Affiche "Jean"
print(mon_dictionnaire["age"])  # Affiche 25
```

### Utilisation des dictionnaires comme des tableaux associatifs
Les dictionnaires peuvent être utilisés comme des tableaux associatifs. Pour cela, il suffit de déclarer un dictionnaire avec des clés qui correspondent aux indices des éléments du tableau associatif et des valeurs qui correspondent aux valeurs des éléments du tableau associatif :
```python
# Déclaration du dictionnaire
mon_dictionnaire = {"0": "Dupont", "1": "Jean", "2": 25}

# Affichage des éléments du tableau associatif
print(mon_dictionnaire["0"])  # Affiche "Dupont"
print(mon_dictionnaire["1"])  # Affiche "Jean"
print(mon_dictionnaire["2"])  # Affiche 25
```

### Utilisation des dictionnaires comme des tableaux à deux dimensions
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
