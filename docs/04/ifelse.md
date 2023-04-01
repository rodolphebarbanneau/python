---
layout: default
title: Structures conditionnelles
parent: Structures de contrôle de flux
nav_order: 4
permalink: /docs/structures/ifelse
---

# Les structures conditionnelles
{: .no_toc }
Les structures conditionnelles sont utilisées pour exécuter des blocs de code en fonction de l'évaluation d'une ou plusieurs conditions. En Python, les structures conditionnelles sont gérées avec les instructions `if`, `elif` et `else`.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## L'instruction `if`
L'instruction `if` permet d'exécuter un bloc de code si une condition est vraie. Voici la syntaxe de base :
```python
if condition:
    # Code exécuté si la condition est vraie
```

La condition peut être une expression qui évalue à `True` ou `False`. Si la condition est `True`, le code indenté sous l'instruction `if` sera exécuté.

## L'instruction `else`
L'instruction `else` est utilisée pour exécuter un bloc de code lorsque la condition dans l'instruction `if` est fausse. Voici la syntaxe de base :
```python
if condition:
    # Code exécuté si la condition est vraie
else:
    # Code exécuté si la condition est fausse
```

Si la condition dans l'instruction `if` est fausse, le code indenté sous l'instruction `else` sera exécuté.

## L'instruction `elif`
L'instruction `elif` est utilisée pour tester plusieurs conditions. Elle est placée après l'instruction `if` et avant l'instruction `else`. Voici la syntaxe de base :
```python
if condition1:
    # Code exécuté si la condition1 est vraie
elif condition2:
    # Code exécuté si la condition2 est vraie
elif condition3:
    # Code exécuté si la condition3 est vraie
else:
    # Code exécuté si aucune condition n'est vraie
```

Si la condition1 est vraie, le code indenté sous l'instruction `if` sera exécuté. Si la condition1 est fausse et que la condition2 est vraie, le code indenté sous la première instruction `elif` sera exécuté. Si la condition1 et condition2 sont fausses et que la condition3 est vraie, le code indenté sous la deuxième instruction `elif` sera exécuté. Si aucune des conditions n'est vraie, le code indenté sous l'instruction `else` sera exécuté.

## Les opérateurs de comparaison
Les opérateurs de comparaison sont utilisés pour évaluer des expressions et retourner un booléen (`True` ou `False`). Voici une liste des opérateurs de comparaison les plus courants en Python :

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `<` | Inférieur à | `2 < 3 = True` |
| `>` | Supérieur à | `2 > 3 = False` |
| `==` | Égal à | `2 == 3 = False` |
| `<=` | Inférieur ou égal à | `2 <= 3 = True` |
| `>=` | Supérieur ou égal à | `2 >= 3 = False` |
| `!=` | Différent de | `2 != 3 = True` |

Exemple :
```python
# Définir une variable
age = 25

# Utiliser les opérateurs de comparaison
if age < 18:
    print("Vous êtes mineur")
elif age >= 18 and age < 65:
    print("Vous êtes majeur")
else:
    print("Vous êtes retraité")
```

## Les opérateurs logiques
Les opérateurs logiques sont utilisés pour combiner deux valeurs booléennes et renvoyer un booléen (`True` ou `False`). Les opérateurs logiques courants en Python sont :

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `and` | ET | `True and True = True` |
| `or` | OU | `True or False = True` |
| `not` | NON | `not True = False` |

Exemple :
```python
# Définir une variable
age = 25

# Utiliser les opérateurs logiques
if age >= 18 and age < 65:
    print("Vous êtes majeur")
```
