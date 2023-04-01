---
layout: default
title: Opérateurs
parent: Variables & Opérateurs
nav_order: 5
permalink: /docs/variables-basic/operators
---

# Les opérateurs
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Qu'est-ce qu'un opérateur ?
Un opérateur est un symbole qui effectue une opération sur des variables ou des valeurs.

## Les opérateurs arithmétiques

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `+` | Addition | `2 + 3 = 5` |
| `-` | Soustraction | `2 - 3 = -1` |
| `*` | Multiplication | `2 * 3 = 6` |
| `/` | Division | `2 / 3 = 0.6666666666666666` |
| `**` | Puissance | `2 ** 3 = 8` |
| `//` | Division entière | `7 // 3 = 2` |
| `%` | Modulo | `7 % 3 = 1` |
| `()` | Parenthèses | `(2 + 3) * 4 = 20` |

Exemple d'utilisation d'opérateurs arithmétiques :
```python
a = 10
b = 3

# Addition
c = a + b
print(c)  # Affiche 13

# Soustraction
c = a - b
print(c)  # Affiche 7

# Multiplication
c = a * b
print(c)  # Affiche 30

# Division
c = a / b
print(c)  # Affiche 3.3333333333333335

# Puissance
c = a ** b
print(c)  # Affiche 1000

# Division entière
c = a // b
print(c)  # Affiche 3

# Modulo
c = a % b
print(c)  # Affiche 1

# Utilisation de parenthèses
c = (a + b) * 2
print(c)  # Affiche 26
```

## Les opérateurs de comparaison

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `<` | Inférieur à | `2 < 3 = True` |
| `>` | Supérieur à | `2 > 3 = False` |
| `==` | Égal à | `2 == 3 = False` |
| `<=` | Inférieur ou égal à | `2 <= 3 = True` |
| `>=` | Supérieur ou égal à | `2 >= 3 = False` |
| `!=` | Différent de | `2 != 3 = True` |

Il est important de noter que l'opérateur d'égalité est `==`, et non `=` qui est utilisé pour assigner une valeur à une variable.

Exemple d'utilisation d'opérateurs de comparaison :
```python
a = 5
b = 10
c = 5

print(a == b)  # False
print(a != b)  # True
print(a < b)   # True
print(a <= c)  # True
print(a >= c)  # True
```

Dans cet exemple, nous avons trois variables `a`, `b` et `c`. Nous utilisons ensuite les opérateurs de comparaison pour comparer les valeurs de ces variables :
- La première instruction (`print(a == b)`) teste si `a` est égal à `b`. Comme `a` et `b` sont différents, cette instruction renvoie `False`.
- La deuxième instruction (`print(a != b)`) teste si `a` est différent de `b`. Comme `a` et `b` sont différents, cette instruction renvoie `True`.
- La troisième instruction (`print(a < b)`) teste si `a` est inférieur à `b`. Comme `a` est inférieur à `b`, cette instruction renvoie `True`.
- La quatrième instruction (`print(a <= c)`) teste si `a` est inférieur ou égal à `c`. Comme `a` est égal à `c`, cette instruction renvoie `True`.
- La cinquième instruction (`print(a >= c)`) teste si `a` est supérieur ou égal à `c`. Comme `a` est égal à `c`, cette instruction renvoie `True`.

## Les opérateurs logiques
Les opérateurs logiques sont utilisés pour combiner deux valeurs booléennes et renvoyer un booléen (`True` ou `False`). Les opérateurs logiques courants en Python sont :

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `and` | ET | `True and True = True` |
| `or` | OU | `True or False = True` |
| `not` | NON | `not True = False` |

L'opérateur `and` renvoie `True` uniquement si les deux valeurs sont `True`. L'opérateur `or` renvoie `True` si au moins une des valeurs est `True`. L'opérateur `not` renvoie l'inverse de la valeur booléenne.

Exemple d'utilisation d'opérateurs logiques :
```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

Dans cet exemple, nous avons deux variables booléennes `a` et `b`. Nous utilisons ensuite les opérateurs logiques pour combiner ces valeurs :
- La première instruction (`print(a and b)`) teste si `a` et `b` sont tous les deux vrais. Comme `b` est faux, cette instruction renvoie `False`.
- La deuxième instruction (`print(a or b)`) teste si `a` ou `b` est vrai. Comme `a` est vrai, cette instruction renvoie `True`.
- La troisième instruction (`print(not a)`) teste si `a` est faux. Comme `a` est vrai, cette instruction renvoie `False`.

Ces opérateurs sont souvent utilisés dans les instructions if et les boucles pour décider de l'exécution ou non d'une partie du code en fonction des valeurs des variables et des résultats des opérations.
