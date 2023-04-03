---
layout: default
title: Fonctions natives
parent: Fonctions
nav_order: 6
permalink: /docs/functions/natives
---

# Les fonctions natives
{: .no_toc }
Le langage Python possède des fonctions natives qui sont définies directement dans le langage et qui sont accessibles partout dans le code. Ces fonctions sont appelées `built-in functions`. Elles sont définies dans le module `builtins` et sont donc accessibles sans avoir besoin d'importer le module.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Fonctions natives de conversion
Les fonctions natives de conversion permettent de convertir une valeur d'un type en un autre type.

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `int(x, base)` | Convertit une valeur en entier | `int("5")` retourne `5` |
| `float(x)` | Convertit une valeur en nombre à virgule flottante | `float("5.5")` retourne `5.5` |
| `bytes(x, encoding, errors)` | Convertit une valeur en octets | `bytes("5", "utf-8")` retourne `b'5'` |
| `str(x)` | Convertit une valeur en chaîne de caractères | `str(5)` retourne `"5"` |
| `bool(x)` | Convertit une valeur en booléen | `bool(5)` retourne `True` |
| `list(x)` | Convertit une valeur en liste | `list("Hello")` retourne `['H', 'e', 'l', 'l', 'o']` |
| `tuple(x)` | Convertit une valeur en tuple | `tuple("Hello")` retourne `('H', 'e', 'l', 'l', 'o')` |
| `set(x)` | Convertit une valeur en ensemble | `set("Hello")` retourne `{'H', 'e', 'l', 'o'}` |
| `dict(x)` | Convertit une valeur en dictionnaire | `dict([("a", 1), ("b", 2)])` retourne `{'a': 1, 'b': 2}` |

## Fonctions natives de manipulation de chaînes de caractères
Les fonctions natives de manipulation de chaînes de caractères permettent de manipuler des chaînes de caractères.

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `len(iterable)` | Retourne la longueur d'un itérable | `len("Hello")` retourne `5` |
| `chr(i)` | Retourne le caractère correspondant à un code ASCII | `chr(65)` retourne `'A'` |
| `ord(c)` | Retourne le code ASCII correspondant à un caractère | `ord('A')` retourne `65` |
| `format(value, format_spec)` | Retourne une chaîne de caractères formatée | `format(123, 'b')` retourne `'1111011'` |
| `str(object)` | Retourne une chaîne de caractères représentant un objet | `str(123)` retourne `'123'` |
| `repr(object)` | Retourne une chaîne de caractères représentant un objet | `repr(123)` retourne `'123'` |

## Fonctions natives de manipulation de listes
Les fonctions natives de manipulation de listes permettent de manipuler des listes.

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `len(iterable)` | Retourne la longueur d'un itérable | `len([1, 2, 3])` retourne `3` |
| `min(iterable, *iterables, key, default)` | Retourne la valeur minimale d'un itérable | `min([1, 2, 3])` retourne `1` |
| `max(iterable, *iterables, key, default)` | Retourne la valeur maximale d'un itérable | `max([1, 2, 3])` retourne `3` |
| `sum(iterable, start)` | Retourne la somme des valeurs d'un itérable | `sum([1, 2, 3])` retourne `6` |
| `sorted(iterable, key, reverse)` | Retourne une liste triée | `sorted([3, 2, 1])` retourne `[1, 2, 3]` |
| `reversed(seq)` | Retourne un itérateur inversé | `reversed([1, 2, 3])` retourne `<list_reverseiterator object>` |
| `enumerate(iterable, start)` | Retourne un itérateur de tuples contenant l'index et la valeur | `enumerate([1, 2, 3])` retourne `<enumerate object>` |
| `zip(*iterables)` | Retourne un itérateur de tuples contenant les valeurs des itérables | `zip([1, 2, 3], [4, 5, 6])` retourne `<zip object>` |
| `any(iterable)` | Retourne `True` si au moins un élément de l'itérable est vrai | `any([1, 2, 3])` retourne `True` |
| `all(iterable)` | Retourne `True` si tous les éléments de l'itérable sont vrais | `all([1, 2, 3])` retourne `True` |
| `filter(function, iterable)` | Retourne un itérateur contenant les éléments de l'itérable pour lesquels la fonction renvoie `True` | `filter(lambda x: x > 2, [1, 2, 3])` retourne `<filter object>` |
| `map(function, *iterables)` | Retourne un itérateur contenant les résultats de la fonction appliquée aux éléments des itérables | `map(lambda x: x * 2, [1, 2, 3])` retourne `<map object>` |
