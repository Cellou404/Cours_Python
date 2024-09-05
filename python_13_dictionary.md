# Python - Les Dictionnaires

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```

## Les Dictionnaires

Les dictionnaires sont utilisés pour stocker des valeurs de données dans des paires clé:valeur.

Un dictionnaire est une collection ordonnée*, modifiable et qui n'autorise pas les doublons.

> À partir de la version 3.7 de Python, les dictionnaires sont ordonnés. Dans Python 3.6 et les versions antérieures, les dictionnaires ne sont pas ordonnés.

Les dictionnaires sont écrits avec des accolades et ont des clés et des valeurs :

**Exemple** :

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

## Éléments du dictionnaire

Les éléments du dictionnaire sont ordonnés, modifiables et ne permettent pas les doublons.

Les éléments du dictionnaire sont présentés sous forme de paires clé:valeur et peuvent être référencés à l'aide du nom de la clé.

**Exemple** :

Imprimez la valeur « marque » du dictionnaire :

```python
print(thisdict["brand"])
```

## Ordonné ou non ordonné ?

> À partir de la version 3.7 de Python, les dictionnaires sont ordonnés. Dans Python 3.6 et les versions antérieures, les dictionnaires ne sont pas ordonnés.

Lorsque nous disons que les dictionnaires sont ordonnés, cela signifie que les éléments ont un ordre défini et que cet ordre ne changera pas.

Non ordonné signifie que les éléments n'ont pas d'ordre défini, vous ne pouvez pas faire référence à un élément en utilisant un index.

## Modifiable

Les dictionnaires sont modifiables, ce qui signifie que nous pouvons modifier, ajouter ou supprimer des éléments après la création du dictionnaire.

Les doublons ne sont pas autorisés
Les dictionnaires ne peuvent pas avoir deux éléments avec la même clé :

**Exemple**:

Les valeurs en double écraseront les valeurs existantes :

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict)
```

## Longueur du dictionnaire

Pour déterminer le nombre d'éléments d'un dictionnaire, utilisez la fonction len() :

```python
print(len(thisdict))
```

## Éléments du dictionnaire - Types de données

Les valeurs des éléments du dictionnaire peuvent être de n'importe quel type de données :

**Exemple** :

Types de données chaîne, int, booléen et liste :

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "isNew": True,
  "colors": ["red", "blue", "green"]
}
print(thisdict)
```

## type()

Du point de vue de Python, les dictionnaires sont définis comme des objets avec le type de données « dict » :

> <class 'dict'>

**Exemple** :

```python
print(type(thisdict))
```

## Le constructeur dict()

Il est également possible d'utiliser le constructeur dict() pour créer un dictionnaire.

**Exemple** :

Utilisation de la méthode dict() pour créer un dictionnaire :

```python
thisdict = dict(
  brand="Ford",
  model="Mustang",
  year=1964,
  isNew=True,
  colors=["red", "blue", "green"]
)
print(thisdict)
```
