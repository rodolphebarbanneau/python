---
layout: default
title: Cheatsheet
parent: Modules et environnement
nav_order: 1
permalink: /docs/modules/cheatsheet
---

# Cheatsheet
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Variables locales, globales et spéciales

### Variables locales
```python
# Déclaration de la variable locale x dans une fonction
def my_function():
    x = 10
    print(x) # Affiche 10
print(x) # Erreur : x n'est pas défini
```

### Variables globales
```python
# Déclaration de la variable globale x
x = 10
print(x) # Affiche 10

# Déclaration de la variable globale x dans une fonction
def my_function():
    global x
    x = 20
my_function()
print(x) # Affiche 20
```

### Variables spéciales
Il existe des variables spéciales qui sont définies par Python et qui sont accessibles dans tous les contextes. Elles sont définies dans le module `builtins` et sont donc accessibles dans tous les modules.

| Variable | Description | Exemple |
| -------- | ----------- | ------- |
| `__name__` | Nom du module | `__main__` |
| `__doc__` | Documentation du module | `Documentation du module` |
| `__package__` | Nom du package | `__main__` |
| `__debug__` | Vaut `True` si le mode debug est activé | `True` |
| `__import__` | Fonction d'importation de modules | `<built-in function __import__>` |
| `__loader__` | Objet de chargement du module | `<class '_frozen_importlib.BuiltinImporter'>` |
| `__spec__` | Objet de spécification du module | `<module 'builtins' (built-in)>` |
| `__file__` | Chemin du fichier | `C:\...\Documents\script.py` |
| `__cached__` | Chemin du fichier cache | `C:\...\Documents\script.py` |
| `__builtins__` | Liste des fonctions natives de Python | `<module 'builtins' (built-in)>` |

## Exécuter du code uniquement lorsqu'un fichier est exécuté directement
Cela permet d'exécuter du code uniquement lorsqu'un fichier est exécuté directement. Par exemple, on peut exécuter des tests unitaires uniquement lorsqu'un fichier est exécuté directement. Si le fichier est importé en tant que module, le code ne sera pas exécuté.
```python
# Exécuter du code uniquement lorsqu'un fichier est exécuté directement
if __name__ == "__main__":
    print("Exécuté directement")
else:
    print("Exécuté en tant que module")
```

## Modules
Les modules sont des fichiers Python qui contiennent des fonctions, des classes, des variables, etc. Ils peuvent être importés dans d'autres modules.

### Importer un module natif ou un module tiers
```python
# Importer le module
import math

# Importer le module et renommer le module
import math as m

# Importer le sous-module
import math.sqrt

# Importer une fonction du module
from math import sqrt

# Importer une fonction du module et renommer la fonction
from math import sqrt as s

# Importer toutes les fonctions du module
from math import *
```

### Importer un module depuis son chemin
```python
# Importe un module dans le même dossier
import .module # Nom du module sans l'extension .py

# Importe un module dans le dossier parent
import ..module # Nom du module sans l'extension .py

# Importe un module dans un sous-dossier
import .sous_dossier.module # Nom du module sans l'extension .py
```

## Environnement courant
L'environnement courant est l'endroit où se trouvent les modules installés. Il est possible d'avoir plusieurs environnements Python sur un même ordinateur. L'environnement courant est défini par la variable d'environnement `PYTHONPATH`.

### Variables d'environnement
Les variables d'environnement sont des variables qui sont accessibles par tous les programmes. Elles sont définies dans le système d'exploitation et sont accessibles par tous les programmes. Elles sont définies dans le dossier `C:\Users\%USERNAME%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.x` sous Windows.

On peut accéder aux variables d'environnement depuis Python avec le module `os` :
```python
# Afficher le chemin de l'environnement courant
import os
print(os.environ["PYTHONPATH"]) 
```

### Pip
Pip est un gestionnaire de paquets pour Python. Il permet d'installer et de gérer des modules tiers. L'installation des modules s'effectue dans l'environnement Python courant depuis l'invite de commande :
```bash
# Installation du module
pip install nom_du_module

# Mise à jour du module
pip install --upgrade nom_du_module

# Désinstallation du module
pip uninstall nom_du_module

# Afficher la liste des modules tiers installés
pip list # Affiche la liste des modules installés
pip freeze # Affiche la liste des modules installés et leurs versions
pip grep nom_du_module # Recherche un module installé
pip show nom_du_module # Affiche les informations du module

# Mettre à jour pip
pip install --upgrade pip
```

## Environnement virtuel
Un environnement virtuel est un environnement Python qui est isolé des autres environnements. Il permet d'installer des modules tiers sans les installer dans l'environnement courant. Il est possible d'avoir plusieurs environnements virtuels sur un même ordinateur.

Nous recommandons d'utiliser l'outil `poetry` pour créer des environnements virtuels. Il permet de créer des environnements virtuels, d'installer des modules tiers, de gérer les dépendances, etc.

### Installation de poetry
```bash
# Installation de poetry
pip install poetry
```

### Créer un environnement virtuel
```bash
# Créer un nouveau project avec son environnement virtuel
poetry new nom_du_projet

# Ou en initialisant un projet existant
poetry init

# Installer les dépendances
poetry install

# Mettre à jour les dépendances
poetry update

# Ajouter une dépendance
poetry add nom_du_module

# Désinstaller les dépendances
poetry remove nom_du_module

# Lancer un shell dans l'environnement virtuel
poetry shell

# Quitter le shell
exit # Ou Ctrl+D
```
