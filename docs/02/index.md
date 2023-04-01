---
layout: default
title: Variables de base, chaînes de caractères et opérateurs
nav_order: 4
---

# Variables de base, chaînes de caractères et opérateurs

![Let's get this started!](../assets/lets_get_this_started.png)

## Cheatsheet
```python
# Déclaration d'une variable en Python
nom_variable = valeur

# Déclaration de variables pour les différents types de données en Python
age = 25 # int
prix = 12.99 # float
nom = "John" # str
est_majeur = True # bool

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

## Partie 1 : Les variables

### Qu'est-ce qu'une variable en Python ?
Une variable est un espace de stockage pour une valeur en Python. Vous pouvez assigner une valeur à une variable à l'aide de l'opérateur `=`. En Python, il n'est pas nécessaire de déclarer une variable avant de l'utiliser.

### Syntaxe de la déclaration d'une variable en Python
En Python, la syntaxe pour déclarer une variable est la suivante :
```python
nom_variable = valeur
```

### Exemples de déclaration de variables en Python
Voici quelques exemples de déclaration de variables en Python :
```python
# Déclaration d'une variable de type int
age = 25

# Déclaration d'une variable de type float
taille = 1.75

# Déclaration d'une variable de type str
nom = "John"

# Déclaration d'une variable de type bool
est_majeur = True

# Déclaration d'une variable sans initialisation
a = None
```

### Règles pour nommer une variable en Python
- Le nom d'une variable doit commencer par une lettre ou un souligné (_).
- Le nom d'une variable ne peut contenir que des lettres, des chiffres et des soulignés.
- Les majuscules et les minuscules sont distinguées en Python.

## Partie 2 : Les types de données de base en Python

### Quels sont les types de données en Python ?

| Type de données | Désignation | Description | Exemple |
| --------------- | ----------- | ----------- | ------- |
| `int` | Entier | Un nombre entier | `1` |
| `float` | Flottant | Un nombre à virgule flottante | `1.0` |
| `str` | Chaîne de caractères | Une chaîne de caractères | `"Hello World"` |
| `bool` | Booléen | Un booléen (vrai ou faux) | `True` |
| `None` | Aucune valeur | Aucune valeur | `None` |


### Déclaration de variables en Python avec les différents types de données
Voici comment déclarer des variables pour les différents types de données en Python :
```python
# Déclaration d'une variable de type int
age = 25

# Déclaration d'une variable de type float
prix = 12.99

# Déclaration d'une variable de type str
nom = "John"

# Déclaration d'une variable de type bool
est_majeur = True
```

## Partie 3 : Les chaînes de caractères en Python
Les chaînes de caractères sont des séquences de caractères délimitées par des guillemets simples (`'`) ou doubles (`"`). En Python, les chaînes de caractères sont des objets de type `str`.

### Déclaration de chaînes de caractères
Vous pouvez déclarer une chaîne de caractères en utilisant des guillemets simples ou doubles, comme ceci :
```python
message1 = 'Bonjour!'
message2 = "Comment ça va?"
```

### Concaténation de chaînes de caractères
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

### Modification de chaînes de caractères
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

### Longueur d'une chaîne de caractères
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

### Accéder aux caractères d'une chaîne
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

## Partie 4 : Les opérateurs en Python

### Qu'est-ce qu'un opérateur en Python ?
Un opérateur est un symbole qui effectue une opération sur des variables ou des valeurs.

### Les opérateurs arithmétiques en Python

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

### Les opérateurs de comparaison en Python

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

### Les opérateurs logiques en Python
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

## Partie 5 : Exercices

### Exercice 1 : Message de bienvenue
>Écrire un programme Python qui demande à l'utilisateur son prénom, son nom et son âge. Le programme doit ensuite afficher un message qui dit "Bonjour [prénoms avec chaque première lettre en majuscule] [nom en majuscule], vous avez [âge] ans".

### Exercice 2 : Calcul de l'IMC
>Écrivez un programme Python qui demande à l'utilisateur son poids (en kg) et sa taille (en m), puis calcule son indice de masse corporelle (IMC) en utilisant la formule IMC = poids / (taille * taille). Affichez ensuite l'IMC avec deux décimales après la virgule. Par exemple, si l'utilisateur saisit un poids de 70 kg et une taille de 1,75 m, le programme devrait afficher "Votre IMC est de 22,86".

### Exercice 3 : Calcul de la moyenne
>Calcul de la moyenne : Écrivez un programme Python qui demande à l'utilisateur trois nombres, puis calcule et affiche leur moyenne avec une précision de deux décimales. Par exemple, si l'utilisateur saisit les nombres 5, 10 et 15, le programme devrait afficher "La moyenne est de 10,00".

### Exercice 4 : Comptage des mots
> Écrire un programme Python qui demande à l'utilisateur de saisir une phrase. Le programme doit compter le nombre d'occurrences de chaque mot dans la phrase et afficher le résultat.
