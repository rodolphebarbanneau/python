---
layout: default
title: Chaînes de caractères
parent: Variables & Opérateurs
nav_order: 4
permalink: /docs/variables-basic/strings
---

# Les chaînes de caractères
{: .no_toc }
Les chaînes de caractères sont des séquences de caractères délimitées par des guillemets simples (`'`) ou doubles (`"`). En Python, les chaînes de caractères sont des objets de type `str`.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Déclaration de chaînes de caractères
Vous pouvez déclarer une chaîne de caractères en utilisant des guillemets simples ou doubles, comme ceci :
```python
message1 = 'Bonjour!'
message2 = "Comment ça va?"
```

## Concaténation de chaînes de caractères
Pour concaténer deux chaînes de caractères, vous pouvez utiliser l'opérateur `+`, comme ceci :
```python
prenom = 'Jean'
nom = 'Dupont'
nom_complet = prenom + ' ' + nom
print(nom_complet) # affiche 'Jean Dupont'
```

Une autre méthode de concaténation consiste à utiliser les accolades `{}` pour insérer des variables dans une chaîne de caractères et la méthode `format()`, comme ceci :
```python
age = 25
message = 'J\'ai {} ans.'.format(age)
print(message) # affiche 'J'ai 25 ans.'
```

Depuis Python 3.6, il est possible d'utiliser les f-strings pour simplifier la concaténation de chaînes de caractères. Il suffit de précéder la chaîne de caractères d'un `f` et d'insérer les variables entre accolades `{}`, comme ceci :
```python
age = 25
message = f'J\'ai {age} ans.'
print(message) # affiche 'J'ai 25 ans.'
```

## Modification de chaînes de caractères
Il est possible de modifier une chaîne de caractères en utilisant des méthodes spécifiques, telles que :
- `lower()` : transforme tous les caractères en minuscules
- `upper()` : transforme tous les caractères en majuscules
- `capitalize()` : met la première lettre en majuscule
- `title()` : met la première lettre de chaque mot en majuscule

Exemple d'utilisation :
```python
nom = 'DUPONT'
nom_lower = nom.lower()
print(nom_lower) # affiche 'dupont'

prenom = 'jean'
prenom_upper = prenom.upper()
print(prenom_upper) # affiche 'JEAN'

nom_complet = 'jean dupont'
nom_complet_capitalize = nom_complet.capitalize()
print(nom_complet_capitalize) # affiche 'Jean dupont'

phrase = 'le python est un langage de programmation'
phrase_title = phrase.title()
print(phrase_title) # affiche 'Le Python Est Un Langage De Programmation'
```

## Longueur d'une chaîne de caractères
La longueur d'une chaîne de caractères peut être obtenue en utilisant la fonction `len()` qui renvoie le nombre de caractères dans la chaîne. Voici un exemple :
```python
chaine = "Bonjour"
longueur = len(chaine)
print("La chaîne", chaine, "a une longueur de", longueur, "caractères.")
```

Cet exemple va afficher le résultat suivant :
```
La chaîne Bonjour a une longueur de 7 caractères.
```

## Accéder aux caractères d'une chaîne
Il est possible d'accéder aux caractères individuels d'une chaîne en utilisant l'index de chaque caractère. Les index commencent à partir de 0 pour le premier caractère et augmentent de 1 pour chaque caractère suivant. Voici un exemple :
```python
chaine = "Hello"
premier_caractere = chaine[0]
deuxieme_caractere = chaine[1]
dernier_caractere = chaine[-1]
print("Le premier caractère de la chaîne est :", premier_caractere)
print("Le deuxième caractère de la chaîne est :", deuxieme_caractere)
print("Le dernier caractère de la chaîne est :", dernier_caractere)
```

Cet exemple va afficher le résultat suivant :
```
Le premier caractère de la chaîne est : H
Le deuxième caractère de la chaîne est : e
Le dernier caractère de la chaîne est : o
```
