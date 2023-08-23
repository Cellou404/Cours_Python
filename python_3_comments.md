# Les commentaires en Python

Les commentaires sont utilisés pour:

- expliquer le code Python
- rendre le code plus lisible
- pour empêcher l'exécution lors du test du code.

## Création d'un commentaire

Les commentaires commencent par un **#**, et Python les ignorera :

```python
#Ceci est un commentaire
print("Hello, World!")
```

Les commentaires peuvent être placés à la fin d'une ligne, et Python ignorera le reste de la ligne :

```python
print("Hello, World!") #Ceci est un commentaire
```

Un commentaire ne doit pas nécessairement être un texte expliquant le code, il peut également être utilisé pour empêcher Python d'exécuter du code :

```python
#print("Hello, World!")
print("Bien le bonjour!")
```

## Commentaires multilignes

Python n'a pas vraiment de syntaxe pour les commentaires multilignes.

Pour ajouter un commentaire multiligne, vous pouvez insérer un # pour chaque ligne comme ceci:

```python
#print("Hello, World!")
#print("Bien le bonjour!")
#print("Ce code ne sera pas exécuter")
```

Ou, pas tout à fait comme prévu, vous pouvez utiliser une chaîne multiligne.

Étant donné que Python ignorera les littéraux de chaîne qui ne sont pas affectés à une variable, vous pouvez ajouter une chaîne multiligne (guillemets triples)
dans votre code et y placer votre commentaire :

```python
"""
Ceci est un commentaire
écrit en plusieurs lignes.
Le code ci-dessous affichera "Bonjour!"
dans la console
"""
print("Bonjour")
```

Tant que la chaîne n'est pas affectée à une variable, Python lira le code, mais l'ignorera ensuite et vous aurez fait un commentaire multiligne.

[Next →](./python_4_variables.md)
