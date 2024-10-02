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

### Éléments du dictionnaire

Les éléments du dictionnaire sont ordonnés, modifiables et ne permettent pas les doublons.

Les éléments du dictionnaire sont présentés sous forme de paires clé:valeur et peuvent être référencés à l'aide du nom de la clé.

**Exemple** :

Imprimez la valeur « marque » du dictionnaire :

```python
print(thisdict["brand"])
```

### Ordonné ou non ordonné ?

> À partir de la version 3.7 de Python, les dictionnaires sont ordonnés. Dans Python 3.6 et les versions antérieures, les dictionnaires ne sont pas ordonnés.

Lorsque nous disons que les dictionnaires sont ordonnés, cela signifie que les éléments ont un ordre défini et que cet ordre ne changera pas.

Non ordonné signifie que les éléments n'ont pas d'ordre défini, vous ne pouvez pas faire référence à un élément en utilisant un index.

### Modifiable

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

### Longueur du dictionnaire

Pour déterminer le nombre d'éléments d'un dictionnaire, utilisez la fonction len() :

```python
print(len(thisdict))
```

### Éléments du dictionnaire - Types de données

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

### type()

Du point de vue de Python, les dictionnaires sont définis comme des objets avec le type de données « dict » :

> <class 'dict'>

**Exemple** :

```python
print(type(thisdict))
```

### Le constructeur dict()

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
## Python - Accéder aux éléments du dictionnaire

### Accès aux éléments

Vous pouvez accéder aux éléments d'un dictionnaire en vous référant au nom de sa clé, entre crochets :

**Exemple**

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
```

Il existe également une méthode appelée `get()` qui donne le même résultat :

```python
x = thisdict.get("model")
```

### Obtenir les clés

La méthode `keys()` renvoie une liste de toutes les clés du dictionnaire.

**Exemple**

Obtenir une liste des clés :

```python
x = thisdict.keys()
```

La liste des clés est une vue du dictionnaire, ce qui signifie que toute modification apportée au dictionnaire sera répercutée dans la liste des clés.

**Exemple**

Ajoutez un nouvel élément au dictionnaire original et constatez que la liste des clés est également mise à jour :

```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.keys()
print(x) #before the change
car["color"] = "white"
print(x) #after the change
```
### Obtenir des valeurs

La méthode values() renvoie une liste de toutes les valeurs du dictionnaire.

```python
x = thisdict.values()
```

La liste des valeurs est une vue du dictionnaire, ce qui signifie que toute modification apportée au dictionnaire sera reflétée dans la liste des valeurs.

**Exemple**

Effectuez une modification dans le dictionnaire original et constatez que la liste des valeurs est également mise à jour :

```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.values()
print(x) #before the change
car["year"] = 2020
print(x) #after the change
```

**Exemple**

Ajoutez un nouvel élément au dictionnaire original et constatez que la liste des valeurs est également mise à jour :

```python
car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.values()
print(x) #before the change
car["color"] = "red"
print(x) #after the change
```

### Obtenir des éléments

La méthode `items()` renvoie chaque élément d'un dictionnaire sous forme de tuples dans une liste.

```python
x = thisdict.items()*
```

La liste renvoyée est une vue des éléments du dictionnaire, ce qui signifie que toute modification apportée au dictionnaire sera reflétée dans la liste des éléments.

**Exemple**

Effectuez une modification dans le dictionnaire d'origine et constatez que la liste des éléments est également mise à jour :

```python
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.items()
print(x) #before the change

car["year"] = 2020
print(x) #after the change
```

**Exemple**

Ajoutez un nouvel élément au dictionnaire original et constatez que la liste des éléments est également mise à jour :

```python
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.items()
print(x) #before the change

car["color"] = "red"
print(x) #after the change
```

### Vérifier si une clé existe

Pour déterminer si une clé spécifiée est présente dans un dictionnaire, utilisez le mot-clé `in` :

**Exemple**

Vérifier si « modèle » est présent dans le dictionnaire :

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")
```

## Modifier les éléments du dictionnaire

## Modifier les valeurs

Vous pouvez modifier la valeur d'un élément spécifique en vous référant à son nom de clé :

**Exemple:**

```python
# change "year" to 2018

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
```

### Mise à jour du dictionnaire*

La méthode `update()` met à jour le dictionnaire avec les éléments de l'argument donné.

L'argument doit être un dictionnaire ou un objet itérable contenant des paires clé/valeur.

**Exemple**

Mettre à jour l'« année » de la voiture en utilisant la méthode `update()` :

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
```
