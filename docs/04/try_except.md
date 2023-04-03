---
layout: default
title: Gestion des erreurs
parent: Structures de contrôle de flux
nav_order: 4
permalink: /docs/structures/try-except
---

# La Gestion des erreurs
{: .no_toc }
La gestion des erreurs en Python permet de gérer les erreurs qui peuvent survenir pendant l'exécution d'un programme et de s'adapter en conséquence. Les erreurs peuvent être dues à divers facteurs, tels que des entrées utilisateur invalides, des erreurs de syntaxe, des erreurs de calcul, des erreurs de fichier, etc.

La gestion des erreurs se fait à l'aide de la structure `try-except`. Cette structure permet de tester un bloc de code pour détecter les erreurs, et de gérer ces erreurs dans un bloc `except`.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Syntaxe
La syntaxe générale de la structure `try-except` est la suivante :
```python
try:
    # Code à tester
except:
    # Code exécuté en cas d'erreur
else:
    # Code exécuté si aucune erreur n'est survenue
finally:
    # Code exécuté à la fin
```

### Bloc `try`
Il contient le code à tester pour détecter les erreurs. Si une exception est levée dans ce bloc, l'exécution du code est interrompue, et la gestion des erreurs prend le relais.

### Bloc `except`
Il contient le code à exécuter en cas d'exception. La clause `except` spécifie le type d'exception que vous souhaitez capturer. Si l'exception levée correspond à ce type, le code dans le bloc `except` est exécuté. Si l'exception ne correspond pas à ce type, elle est propagée à l'extérieur de la structure `try-except`, et le programme peut s'arrêter si aucune autre gestion d'erreur n'est mise en place. Il est également possible d'utiliser plusieurs clauses `except` pour capturer différents types d'exceptions, ou une clause `except` sans spécifier le type d'exception pour capturer toutes les exceptions.

### Bloc `else`
Il contient le code à exécuter si aucune exception n'est levée dans le bloc `try`.

### Bloc `finally`
Il contient le code à exécuter à la fin, que l'exception soit levée ou non.

## Exemples pratiques

### Division par zéro
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Division par zéro impossible !")
```
Une exception de type `ZeroDivisionError` est levée car on essaie de diviser un nombre par zéro. La gestion des erreurs permet de capturer cette exception et d'afficher un message d'erreur approprié.

### Ouverture d'un fichier inexistant
```python
try:
    f = open("monfichier.txt", "r")
    contenu = f.read()
    f.close()
except FileNotFoundError:
    print("Le fichier spécifié est introuvable !")
```
Le programme essaie d'ouvrir un fichier qui n'existe pas. La gestion des erreurs permet de capturer l'exception de type `FileNotFoundError` et d'afficher un message d'erreur approprié.

### Erreur sans type d'exception
```python
try:
    x = 1 / 0
except:
    print("Une erreur s'est produite !")
```
La clause `except` ne spécifie pas le type d'exception, ce qui permet de capturer toutes les exceptions éventuelles et d'afficher un message d'erreur générique.

### Plusieurs types d'exceptions
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Division par zéro impossible !")
except:
    print("Une erreur s'est produite !")
```
Il est possible d'utiliser plusieurs clauses `except` pour capturer différents types d'exceptions. Dans cet exemple, la clause `except` sans type d'exception permet de capturer toutes les exceptions non gérées par la clause `except ZeroDivisionError`. Si on inverse les deux clauses `except`, la clause `except ZeroDivisionError` ne sera jamais exécutée car elle ne peut pas capturer l'exception de type `TypeError`. Dans ce cas, la clause `except` sans type d'exception capturera l'exception de type `TypeError` et affichera le message d'erreur générique.

### Utilisation du bloc `else` et du bloc `finally`
```python
try:
    x = 10 / 2
except ZeroDivisionError:
    print("Division par zéro impossible !")
else:
    print("Le résultat est :", x)
finally:
    print("Fin de l'exécution")
```
Il est également possible d'utiliser la clause `else` pour exécuter du code après le bloc `try` si aucune exception n'a été levée, et la clause `finally` pour exécuter de manière systématique du code, qu'il y ait eu ou non une exception.

Dans cet exemple, la division ne soulève pas d'exception, donc le code dans la clause `else` est exécuté, et le résultat est affiché. Le code dans la clause `finally` est également exécuté, que l'exception ait été levée ou non.

## Conclusion
En résumé, la gestion des erreurs en Python est une technique essentielle pour gérer les erreurs pouvant survenir lors de l'exécution d'un programme. La structure `try-except` permet de capturer les exceptions et de les gérer de manière appropriée, en affichant des messages d'erreur adaptés ou en exécutant des actions spécifiques. Il est également possible d'utiliser les clauses `else` et `finally` pour exécuter du code supplémentaire en fonction du déroulement de l'exécution.
