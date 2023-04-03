---
layout: default
title: Exercices
parent: Fonctions
nav_order: 8
permalink: /docs/functions/exercices
---

# Exercices

## Exercice 1 : Dictionnaire de mots
> Écrire une fonction qui prend en entrée une liste de mots et renvoie un dictionnaire où chaque clé est un mot et la valeur associée est le nombre de fois où ce mot apparaît dans la liste. Cette fonction doit utiliser une fonction callback pour compter le nombre d'occurrences d'un mot dans une liste.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/05/exercises/01.py)

## Exercice 2 : Somme des nombres pairs
> Écrire un programme Python qui renvois la somme de tous les nombres pairs précédent un nombre donné. La fonction doit être récursive.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/05/exercises/02.py)

## Exercice 3 :  
> Supposons que vous travaillez pour une entreprise de vente en ligne. Vous avez été chargé de créer un programme qui permet de calculer le prix total d'une commande, en fonction des articles commandés et de leur prix unitaire. Le programme doit être capable de prendre en compte différents types d'articles, chacun ayant un prix unitaire différent. De plus, pour certaines promotions spéciales, des articles peuvent être offerts si certaines conditions sont remplies.

> Voici les informations dont vous disposez :
> - Les articles sont représentés sous forme de dictionnaires, avec leur nom et leur prix unitaire.
> - Les promotions sont également représentées sous forme de dictionnaires, avec les articles concernés, la quantité minimale à commander pour bénéficier de la promotion, et la quantité offerte.

> Votre tâche consiste à créer une fonction `calculer_prix_total(commande, promotions)` qui prend en entrée :
> - Une liste de dictionnaires représentant la commande (chaque dictionnaire contenant le nom et la quantité de chaque article commandé).
> - Une liste de dictionnaires représentant les promotions.

> La fonction doit retourner le prix total de la commande, en tenant compte des articles commandés et des promotions applicables. Voici un exemple d'utilisation de la fonction :

```python	
articles = [
    {'nom': 'chaussures', 'quantite': 2},
    {'nom': 'chemise', 'quantite': 1},
    {'nom': 'pantalon', 'quantite': 1}
]

promotions = [
    {'articles': ['chaussures'], 'quantite_min': 2, 'quantite_offerte': 1},
    {'articles': ['chemise', 'pantalon'], 'quantite_min': 2, 'quantite_offerte': 1}
]

prix_total = calculer_prix_total(articles, promotions)
print(prix_total)
```

> Ce code devrait afficher le prix total de la commande, en tenant compte des promotions applicables.

[Solution](https://github.com/rodolphebarbanneau/python/blob/main/docs/05/exercises/03.py)
