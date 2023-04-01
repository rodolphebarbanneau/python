---
layout: default
title: Tuples `tuple`
parent: Variables avancées
nav_order: 3
permalink: /docs/variables-advanced/tuples
---

# Les tuples
{: .no_toc }
Les tuples sont des structures de données similaires aux listes, mais qui ont quelques différences importantes. Les tuples sont immuables, ce qui signifie qu'ils ne peuvent pas être modifiés après leur création. En outre, les tuples peuvent être utilisés comme clés dans les dictionnaires, ce qui n'est pas possible avec les listes.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Création de tuples
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

## Accès aux éléments des tuples
Les éléments des tuples sont accessibles de la même manière que pour les listes, en utilisant des index. Par exemple :
```python
mon_tuple = (1, 2, 3)
print(mon_tuple[0]) # affiche 1
print(mon_tuple[1]) # affiche 2
print(mon_tuple[2]) # affiche 3
```

Il n'est cependant pas possible de modifier les éléments d'un tuple après sa création.

## Utilisations avancées des tuples
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
