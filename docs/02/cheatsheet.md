
---
layout: default
title: Cheatsheet
parent: Variables & Opérateurs
nav_order: 1
permalink: /docs/variables-basic/cheatsheet
---

# Cheatsheet
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Variables & Types de données
```python
# Déclaration d'une variable en Python
nom_variable = valeur

# Déclaration de variables pour les différents types de données en Python
age = 25 # int
prix = 12.99 # float
nom = "John" # str
est_majeur = True # bool
```

## Chaînes de caractères
```python
# Déclaration de chaînes de caractères
message1 = 'Bonjour!'
message2 = "Comment ça va?"

# Concaténation de chaînes de caractères
prenom = 'Jean'
nom = 'Dupont'
nom_complet = prenom + ' ' + nom
message = 'J\'ai {} ans.'.format(age) # \ permet d'échapper le caractère '
message_f = f'J\'ai {age} ans.'

# Modification de chaînes de caractères
nom_lower = nom.lower()
prenom_upper = prenom.upper()
nom_complet_capitalize = nom_complet.capitalize()
phrase_title = phrase.title()

# Longueur d'une chaîne de caractères
chaine = "Bonjour"
longueur = len(chaine)

# Accéder aux caractères d'une chaîne de caractères
chaine = "Hello"
premier_caractere = chaine[0]
deuxieme_caractere = chaine[1]
dernier_caractere = chaine[-1]
```

## Opérateurs
```python
# Opérateurs arithmétiques
a = 10
b = 3
c = a + b # 13
c = a - b # 7
c = a * b # 30
c = a / b # 3.3333333333333335
c = a ** b # 1000
c = a // b # 3
c = a % b # 1
c = (a + b) * 2 # 26

# Opérateurs de comparaison
a = 5
b = 10
c = 5
a == b # False
a != b # True
a < b # True
a <= c # True
a >= c # True

# Opérateurs logiques
a = True
b = False
a and b # False
a or b # True
not a # False
```
