---
layout: default
title: Fichiers
nav_order: 9
has_children: true
permalink: /docs/files
---

# Fonctions
{: .no_toc }

![](../assets/.png)

## Cheatsheet
{: .no_toc }

### Lecture et écriture de fichiers

#### Ouverture d'un fichier
L'ouverture d'un fichier se fait avec la fonction `open()`. Cette fonction prend en paramètre le chemin du fichier et le mode d'ouverture du fichier (combinaison entre les 2 modes suivants).

| Mode 1 | Description |
| ------ | ----------- |
| `r` | Lecture (défaut) |
| `w` | Écriture (écrase le fichier s'il existe déjà) |
| `a` | Écriture (ajout à la fin du fichier) |
| `x` | Création (erreur si le fichier existe déjà) |

| Mode 2 | Description |
| ------ | ----------- |
| `t` | Mode texte (défaut)
| `b` | Mode binaire |
| `+` | Lecture et écriture |

```python
# Ouverture du fichier en mode lecture
fichier = open('fichier.txt', 'r')

# Ouverture du fichier en mode écriture (écrase le fichier s'il existe déjà)
fichier = open('fichier.txt', 'w')

# Ouverture du fichier en mode ajout à la fin
fichier = open('fichier.txt', 'a')

# Ouverture du fichier en mode lecture et écriture
fichier = open('fichier.txt', 'r+')

# Ouverture du fichier en mode lecture et écriture (écrase le fichier s'il existe déjà)
fichier = open('fichier.txt', 'w+')

# Ouverture du fichier en mode lecture et écriture à la fin
fichier = open('fichier.txt', 'a+')
```

#### Fermeture d'un fichier
```python
fichier.close() # Fermeture du fichier
```

#### Lecture d'un fichier
```python
# Lire le contenu du fichier
contenu = fichier.read()

 # Lire le contenu du fichier en spécifiant le nombre de caractères à lire
contenu = fichier.read(10)

 # Lire une ligne du fichier
contenu = fichier.readline()

# Lire une ligne du fichier en spécifiant le nombre de caractères à lire
contenu = fichier.readline(10)

# Lire toutes les lignes du fichier (retourne une liste)
contenu = fichier.readlines()

# Lecture du fichier ligne par ligne
for ligne in fichier:
    print(ligne)
```

#### Ecriture dans un fichier
```python
# Écrire une chaîne de caractères dans le fichier
fichier.write("Hello World")

# Écrire une liste de chaînes de caractères dans le fichier
fichier.writelines(["Hello", "World"])
```

#### Positionnement du curseur
```python
# Positionnement du curseur au début du fichier
fichier.seek(0)

# Positionnement du curseur au début du fichier
fichier.seek(0, 0) # 0 = début du fichier

# Positionnement du curseur à la position 10 relative à la position actuelle
fichier.seek(10, 1) # 1 = position actuelle

# Positionnement du curseur à la fin du fichier
fichier.seek(0, 2) # 2 = fin du fichier
```

### Gestion des erreurs

#### Gestion des erreurs avec `try` et `except`
```python
try:
    fichier = open('fichier.csv', 'r')
except FileNotFoundError:
    print("Le fichier n'existe pas")
except PermissionError:
    print("Vous n'avez pas la permission d'accéder au fichier")
except:
    print("Une erreur est survenue")
else:
    print("Le fichier a été ouvert avec succès")
finally:
    print("Fin du programme")
```

#### Gestion des erreurs avec `with`
```python
with open('fichier.csv', 'r') as fichier:
    print("Le fichier a été ouvert avec succès")
```

### Utilisation de fichiers CSV

#### Lecture d'un fichier CSV
```python
import csv

with open('fichier.csv', newline='') as csvfile:
    reader = csv.reader(csvfile, delimiter=';', quotechar='"')
    for row in reader:
        print(', '.join(row))
```

#### Écriture dans un fichier CSV
```python
import csv

with open('fichier.csv', 'w', newline='') as csvfile:
    writer = csv.writer(csvfile, delimiter=';', quotechar='"', quoting=csv.QUOTE_MINIMAL)
    writer.writerow(['Nom', 'Prénom', 'Age'])
    writer.writerow(['Doe', 'John', '30'])
    writer.writerow(['Doe', 'Jane', '28'])
```


### Utilisation de fichiers JSON

#### Lecture d'un fichier JSON
```python
import json

with open('fichier.json', 'r') as jsonfile:
    data = json.load(jsonfile)
    print(data)
```

#### Écriture dans un fichier JSON
```python
import json

data = {
    "name": "John Doe",
    "age": 30,
    "married": True,
    "divorced": False,
    "children": ("Ann", "Billy"),
    "pets": None,
    "cars": [
        {"model": "BMW 230", "mpg": 27.5},
        {"model": "Ford Edge", "mpg": 24.1}
    ]
}

with open('fichier.json', 'w') as jsonfile:
    json.dump(data, jsonfile)
```
