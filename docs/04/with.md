---
layout: default
title: Structure `with`
parent: Structures de contrôle de flux
nav_order: 5
permalink: /docs/structures/try-except
---

# La structure `with`
{: .no_toc }
La structure `with` permet de gérer les ressources de manière automatique. Elle permet par exemple de fermer automatiquement les fichiers ouverts, de fermer automatiquement les connexions à la base de données, etc... Elle est utilisée avec des objets qui implémentent la méthode `__enter__` et `__exit__` (cf. les classes pour plus de détails).

Elle permet également de simplifier le code et de le rendre plus lisible en gérant les erreurs de manière automatique.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Syntaxe
La syntaxe générale de la structure `with` est la suivante :
```python
with expression as variable:
    # Code à exécuter
```

## Exemples pratiques

### Ouverture d'un fichier
```python
with open("fichier.txt", "r") as fichier:
    # Code à exécuter
```

### Connexion à une base de données
```python
with sqlite3.connect("ma_base.db") as connexion:
    # Code à exécuter
```
