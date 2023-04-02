---
layout: default
title: Exercices
parent: Structures de contrôle de flux
nav_order: 6
permalink: /docs/structures/exercices
---

# Exercices

## Exercice 1 : Calculatrice
>Ecrire un programme Python qui demande à l'utilisateur d'entrer un nombre et de choisir un mode de calcul parmi l'addition, la soustraction, la multiplication et la division. Ensuite, le programme demande à l'utilisateur un deuxième nombre et affiche le résultat de l'opération sélectionnée.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/04/exercises/01.py)

## Exercice 2 : Palindrome
>Ecrire un programme Python qui demande à l'utilisateur de saisir une chaîne de caractères. Le programme doit vérifier si la chaîne est un palindrome (c'est-à-dire si elle peut être lue de la même façon de gauche à droite et de droite à gauche). Si la chaîne est un palindrome, le programme doit afficher un message de confirmation. Sinon, le programme doit afficher un message d'erreur.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/04/exercises/02.py)

## Exercice 3 : Jeu du nombre mystère
>Ecrire un programme Python qui génère un nombre aléatoire entre 1 et 100.
```python
import random
nombre = random.randint(1, 100)
```
>Ensuite, le programme demande à l'utilisateur de deviner le nombre. Si l'utilisateur devine le nombre correctement, le programme affiche un message de félicitations. Sinon, le programme donne des indices pour aider l'utilisateur à deviner le nombre (plus grand ou plus petit que le nombre choisi). Le programme doit continuer à demander des réponses à l'utilisateur jusqu'à ce qu'il devine correctement. Le nombre de tentatives doit être affiché à la fin du jeu.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/04/exercises/03.py)
