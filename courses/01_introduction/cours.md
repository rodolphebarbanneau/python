# Semaine 1 : Introduction à Python

## Partie 1 : Présentation de Python

### Qu'est-ce que Python ?
Python est un langage de programmation interprété, orienté objet et facile à lire et écrire. Il est souvent utilisé pour le développement de logiciels, de sites web, d'outils d'analyse de données et d'intelligence artificielle.

### Pourquoi Python est-il un langage de programmation populaire ?
Python est populaire pour plusieurs raisons :
- Il est facile à apprendre et à comprendre
- Il a une syntaxe claire et concise
- Il est utilisé dans de nombreuses industries, notamment la science des données, l'intelligence artificielle et le développement web
- Il possède une large communauté d'utilisateurs qui fournissent des bibliothèques et des modules utiles

### Applications courantes de Python
Python est utilisé dans de nombreuses industries, notamment :
- La science des données et l'analyse de données
- L'intelligence artificielle et l'apprentissage automatique
- Le développement web et les applications de bureau
- L'automatisation de tâches et de processus

### Présentation de la syntaxe Python
La syntaxe Python est simple et facile à lire. Les instructions sont séparées par des sauts de ligne et l'indentation est importante pour définir les blocs de code. Python utilise également des bibliothèques et des modules pour ajouter des fonctionnalités et des capacités supplémentaires.

## Partie 2 : Installation de Python et VS Code

### Installation de Python sur Windows
- Allez sur le site officiel de Python : https://www.python.org/downloads/
- Téléchargez la dernière version de Python pour Windows
- Exécutez le programme d'installation et suivez les instructions à l'écran

### Installation de VS Code sur Windows
- Allez sur le site officiel de VS Code : https://code.visualstudio.com/download
- Téléchargez la dernière version de VS Code pour Windows
- Exécutez le programme d'installation et suivez les instructions à l'écran

### Configuration d'un environnement de développement Python avec VS Code
- Ouvrez VS Code
- Installez l'extension Python pour VS Code
- Créez un nouveau dossier pour vos projets Python
- Créez un nouveau fichier Python (.py) dans ce dossier
- Ajoutez votre code Python dans ce fichier

## Partie 3 : Concepts de base de la programmation

### Les variables
Une variable est un espace de stockage pour une valeur. En Python, vous pouvez déclarer et initialiser une variable comme ceci :
```python
nom_variable = valeur
```

### Les types de données
Les types de données courants en Python sont :
- Les nombres :
    - `int` : Nombre entier
    - `float` : Nombre à virgule flottante
- Le texte :
    - `str` : Pour "string" (chaîne de caractères)
- Les booléens :
    - `True` : Vrai
    - `False` : Faux
- Les dates :
    - `datetime` : Pour "date and time" (date et heure)


### Les opérateurs
Les opérateurs courants en Python sont :
- Les opérateurs arithmétiques :

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

- Les opérateurs de comparaison :

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `<` | Inférieur à | `2 < 3 = True` |
| `>` | Supérieur à | `2 > 3 = False` |
| `==` | Égal à | `2 == 3 = False` |
| `<=` | Inférieur ou égal à | `2 <= 3 = True` |
| `>=` | Supérieur ou égal à | `2 >= 3 = False` |
| `!=` | Différent de | `2 != 3 = True` |

- Les opérateurs logiques :

| Opérateur | Description | Exemple |
| --------- | ----------- | ------- |
| `and` | ET | `True and True = True` |
| `or` | OU | `True or False = True` |
| `not` | NON | `not True = False` |

### Les fonctions

#### Définition d'une fonction
Une fonction est un bloc de code qui exécute une tâche spécifique. En Python, vous pouvez définir une fonction comme ceci :
```python
def nom_fonction(parametre1, parametre2):
    # Code exécuté par la fonction
    print(parametre1 + parametre2)
```

#### Appel d'une fonction

Une fonction est appelée en utilisant son nom suivi de parenthèses :
```python
nom_fonction(parametre1, parametre2)
```

#### Fonctions natives
Python possède de nombreuses fonctions natives qui peuvent être utilisées pour effectuer des tâches courantes. Parmi les fonctions natives les plus courantes, nous retrouvons :

| Fonction | Description | Exemple |
| -------- | ----------- | ------- |
| `print()` | Affiche un message à l'écran | `print('Hello World')` |
| `input()` | Demande à l'utilisateur d'entrer une valeur | `input('Entrez une valeur : ')` |
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

### Les structures de contrôle de flux
Les structures de contrôle de flux sont utilisées pour décider de l'exécution ou non d'une partie de votre code. Les structures de contrôle de flux courantes en Python sont :
- Les instructions if/else :
```python
if condition:
    # Code exécuté si la condition est vraie
    print('La condition est vraie')
else:
    # Code exécuté si la condition est fausse
    print('La condition est fausse')
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
    print('La condition est vraie')
```

## Partie 4 : Exemples pratiques

Écriture d'un programme Python simple qui demande à l'utilisateur son nom et affiche un message de bienvenue :
```python
# Demander le nom de l'utilisateur
nom_utilisateur = input('Entrez votre nom : ')

# Afficher un message de bienvenue
print('Bonjour, ' + nom_utilisateur + '!')
```

Écriture d'un programme Python qui calcule l'aire d'un cercle en fonction du rayon :
```python
# Demander le rayon du cercle
rayon = float(input('Entrez le rayon du cercle : '))

# Calculer l'aire du cercle
aire = 3.14 * (rayon ** 2)

# Afficher l'aire du cercle
print('Aire du cercle : ', aire)
```

## Partie 5 : Ressources supplémentaires

Sites web utiles pour apprendre Python :
- https://www.python.org/
- https://docs.python.org/3/tutorial/
- https://realpython.com/
- https://stackoverflow.com/questions/tagged/python

Livres recommandés sur Python :
- "Learning Python" de Mark Lutz
- "Python Crash Course" d'Eric Matthes
- "Python for Data Analysis" de Wes McKinney

## Partie 6 : Exercices

### Exercice 1
Écrire un programme Python qui demande à l'utilisateur son nom et son âge et affiche un message de bienvenue avec ces informations. Si l'utilisateur a moins de 18 ans, afficher un message d'erreur. Si l'utilisateur a plus de 18 ans, afficher un message de succès.

### Exercice 2
Écrire un programme Python qui demande à l'utilisateur de saisir un nombre et affiche le carré de ce nombre.

### Exercice 3
Ecire un programme Python qui demande à l'utilisateur de saisir un nombre et indique si ce nombre est pair ou impair.
