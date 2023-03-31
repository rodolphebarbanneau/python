# Semaine 1 : Concepts de base de la programmation

<p align="center">
  <img src="../assets/python_natives.png" alt="Guy learning Python..." width="500"
</p>

## Partie 1 : Les variables
Une variable est un espace de stockage pour une valeur. En Python, vous pouvez déclarer et initialiser une variable comme ceci :
```python
nom_variable = valeur
```

### Les types de données de base

| Type de données | Désignation | Description | Exemple |
| --------------- | ----------- | ----------- | ------- |
| `int` | Entier | Un nombre entier | `1` |
| `float` | Flottant | Un nombre à virgule flottante | `1.0` |
| `str` | Chaîne de caractères | Une chaîne de caractères | `"Hello World"` |
| `bool` | Booléen | Un booléen (vrai ou faux) | `True` |
| `datetime` | Date et heure | Une date et une heure | `datetime.datetime(2020, 1, 1, 0, 0)` |
| `None` | Aucune valeur | Aucune valeur | `None` |

### Les types de données avancées

| Type de données | Désignation | Description | Exemple |
| --------------- | ----------- | ----------- | ------- |
| `list` | Liste | Une liste de valeurs, ordonnée et modifiable | `["a", "b", "c"]` |
| `tuple` | Tuple | Une liste de valeurs, ordonnée et non modifiable | `("a", "b", "c")` |
| `set` | Ensemble | Une liste de valeurs, non ordonnée et non modifiable | `{"a", "b", "c"}` |
| `dict` | Dictionnaire | Une liste de valeurs, non ordonnée et modifiable | `{"a": 1, "b": 2, "c": 3}` |

## Partie 2 : Les opérateurs

### Les opérateurs arithmétiques

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

### Les opérateurs de comparaison

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `<` | Inférieur à | `2 < 3 = True` |
| `>` | Supérieur à | `2 > 3 = False` |
| `==` | Égal à | `2 == 3 = False` |
| `<=` | Inférieur ou égal à | `2 <= 3 = True` |
| `>=` | Supérieur ou égal à | `2 >= 3 = False` |
| `!=` | Différent de | `2 != 3 = True` |

### Les opérateurs logiques

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `and` | ET | `True and True = True` |
| `or` | OU | `True or False = True` |
| `not` | NON | `not True = False` |

## Partie 3 : Les structures de contrôle de flux
Les structures de contrôle de flux sont utilisées pour décider de l'exécution ou non d'une partie de votre code. Les structures de contrôle de flux courantes en Python sont :
- Les instructions if/else :
```python
if condition:
    # Code exécuté si la condition est vraie
    print("La condition est vraie")
else:
    # Code exécuté si la condition est fausse
    print("La condition est fausse")
```
- Les boucles for :
```python
for element in sequence:
    # Code exécuté pour chaque élément de la séquence
    print(element)
```
- Les boucles while :
```python
while condition:
    # Code exécuté tant que la condition est vraie
    print("La condition est vraie")
```

## Partie 4 : Les fonctions

### Définition d'une fonction
Une fonction est un bloc de code qui exécute une tâche spécifique. En Python, vous pouvez définir une fonction comme ceci :
```python
def nom_fonction(parametre1, parametre2):
    # Code exécuté par la fonction
    print(parametre1 + parametre2)
```

### Appel d'une fonction

Une fonction est appelée en utilisant son nom suivi de parenthèses :
```python
nom_fonction(parametre1, parametre2)
```

### Fonctions natives
Python possède de nombreuses fonctions natives qui peuvent être utilisées pour effectuer des tâches courantes. Parmi les fonctions natives les plus courantes, nous retrouvons :

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `print()` | Affiche un message à l'écran | `print("Hello World")` |
| `input()` | Demande à l'utilisateur d'entrer une valeur | `input("Entrez une valeur : ")` |
| `type()` | Retourne le type d'une variable | `type(2)` |
| `int()` | Convertit une valeur en nombre entier | `int('2')` |
| `float()` | Convertit une valeur en nombre à virgule flottante | `float('2.5')` |
| `str()` | Convertit une valeur en chaîne de caractères | `str(2)` |
| `bool()` | Convertit une valeur en booléen | `bool(1)` |
| `datetime()` | Convertit une valeur en date et heure | `datetime(2020, 1, 1)` |
| `round()` | Arrondit un nombre à un nombre de décimales donné | `round(2.5)` |
| `abs()` | Retourne la valeur absolue d'un nombre | `abs(-2)` |
| `pow()` | Retourne la puissance | `pow(2, 3)` |
| `help()` | Affiche l'aide d'une fonction | `help(print)` |

## Partie 5 : Exemples pratiques

Écriture d'un programme Python simple qui demande à l'utilisateur son nom et affiche un message de bienvenue :
```python
# Demander le nom de l'utilisateur
nom_utilisateur = input("Entrez votre nom : ")

# Afficher un message de bienvenue
print("Bonjour, " + nom_utilisateur + "!")
```

Écriture d'un programme Python qui calcule l'aire d'un cercle en fonction du rayon :
```python
# Demander le rayon du cercle
rayon = float(input("Entrez le rayon du cercle : "))

# Calculer l'aire du cercle
aire = 3.14 * (rayon ** 2)

# Afficher l'aire du cercle
print("Aire du cercle : ", aire)
```

## Partie 6 : Exercices

### Exercice 1
```
Écrire un programme Python qui demande à l'utilisateur son nom et son âge et affiche un message de bienvenue avec ces informations. Si l'utilisateur a moins de 18 ans, afficher un message d'erreur. Si l'utilisateur a plus de 18 ans, afficher un message de succès.
```

### Exercice 2
```
Écrire un programme Python qui demande à l'utilisateur de saisir un nombre et affiche le carré de ce nombre.
```

### Exercice 3
```
Ecire un programme Python qui demande à l'utilisateur de saisir un nombre et indique si ce nombre est pair ou impair.
```
