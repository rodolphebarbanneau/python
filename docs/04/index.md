---
layout: default
title: Structures de contrôle de flux
nav_order: 6
has_children: true
permalink: /docs/structures
---

# Structures de contrôle de flux
{: .no_toc }

![If vs if else](../assets/if-vs-if-else.png)

## Cheatsheet
{: .no_toc }

### Boucles `for`
Utilisation pour répéter un bloc d'instructions un nombre défini de fois.
```python
for i in range(5): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 0 à 4

for i in range(5, 10): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 5 à 9

for i in range(5, 10, 2): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 5 à 9 par pas de 2

for i in range(10, 5, -1): # Boucle `for` sur une plage de nombres
    print(i) # Afficher les nombres de 10 à 6
```

### Boucles `while`
Utilisation pour répéter un bloc d'instructions tant qu'une condition est vraie.
```python
i = 0 # Initialisation d'une variable
while i < 5: # Boucle `while` tant que la condition est vraie
    print(i) # Afficher les nombres de 0 à 4
    i += 1 # Incrémenter la variable
    
    if i == 3: # Condition
        break # Arrêter la boucle
```

### Conditions
Utilisation pour exécuter un bloc d'instructions si une condition est vraie.
```python
if 1 < 2: # Condition
    print("1 est inférieur à 2") # Afficher le message
elif 1 > 2: # Sinon si
    print("1 est supérieur à 2") # Afficher le message
else: # Sinon
    print("1 est égal à 2") # Afficher le message
```

### Gestions d'erreurs
Utilisation pour gérer les erreurs de manière automatique.
```python
try: # Essayer d'exécuter le code
    1 / 0 # Division par zéro
except ZeroDivisionError: # Si une erreur de type `ZeroDivisionError` est levée
    print("Division par zéro") # Afficher le message
except: # Si une autre erreur est levée
    print("Une autre erreur est survenue") # Afficher le message
else: # Si aucune erreur n'est levée
    print("Aucune erreur n'est survenue") # Afficher le message
finally: # Quoi qu'il arrive
    print("Fin du programme") # Afficher le message
```

### Structure `with`
Utilisation pour gérer les ressources de manière automatique.
```python
with open("fichier.txt", "r") as fichier: # Ouverture d'un fichier
    # Code à exécuter

with sqlite3.connect("ma_base.db") as connexion: # Connexion à une base de données
    # Code à exécuter
```
