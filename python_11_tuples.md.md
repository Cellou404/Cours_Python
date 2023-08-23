# Python - Tuples

```python
mytuple = ("apple", "banana", "cherry")
```

## Tuple

Les tuples sont utilisés pour stocker plusieurs éléments dans une seule variable.

Tuple est l'un des 4 types de données intégrés à Python utilisés pour stocker des collections de données, les 3 autres sont **List**, **Set** et **Dictionary**, tous avec des qualités et une utilisation différentes.

Un tuple est une collection ordonnée et immuable.

Les tuples sont écrits entre parenthèses.

**Exemple**

Créer un tuple

```python
thistuple = ("apple", "banana", "cherry")  
print(thistuple)
```

### Éléments de tuple

Les éléments de tuple sont ordonnés, non modifiables et autorisent les valeurs en double.

Les éléments de tuple sont indexés, le premier élément a l'index [0], le deuxième élément a l'index [1], etc.

### Ordonné

Lorsque nous disons que les tuples sont ordonnés, cela signifie que les éléments ont un ordre défini et que cet ordre ne changera pas.

### Non modifiable

Les tuples sont immuables, ce qui signifie que nous ne pouvons pas modifier, ajouter ou supprimer des éléments après la création du tuple.

### Autorise les doublons

Puisque les tuples sont indexés, ils peuvent avoir des éléments avec la même valeur :

**Exemple**

Les tuples acceptent les doublons

```python
thistuple = ("apple", "banana", "cherry", "apple", "cherry")  
print(thistuple)
```

### Longueur de tuple

Pour déterminer le nombre d'éléments d'un tuple, utilisez la fonction `len() `:

**Exemple**

Imprimer le nombre d'éléments dans le tuple :

```python
thistuple = ("apple", "banana", "cherry")  
print(len(thistuple))
```

### Créer un tuple avec un élément

Pour créer un **tuple** avec un seul élément, vous devez ajouter une virgule après l'élément, sinon Python ne le reconnaîtra pas comme un tuple.

**Exemple**

Un tuple d'élément, rappelez-vous la virgule :

```python
thistuple = ("apple",)  
print(type(thistuple))  
  
#NOT a tuple  
thistuple = ("apple")  
print(type(thistuple))
```

### Éléments de tuple - Types de données

Les éléments de tuple peuvent être de n'importe quel type de données :

**Exemple**

Types de données chaîne, int et booléen :

```python
tuple1 = ("apple", "banana", "cherry")  
tuple2 = (1, 5, 7, 9, 3)  
tuple3 = (True, False, False)
```

Un tuple peut contenir différents types de données :

**Exemple**

Un tuple avec des chaînes, des entiers et des valeurs booléennes :

```python
tuple1 = ("abc", 34, True, 40, "male")
```

### type()

Du point de vue de Python, les tuples sont définis comme des objets avec le type de données 'tuple' :

`<classe 'tuple'>`

**Exemple**

Quel est le type de données d'un tuple ?

```python
mytuple = ("apple", "banana", "cherry")  
print(type(mytuple))
```

### Le constructeur tuple()

Il est également possible d'utiliser le constructeur `tuple()` pour créer un tuple.

**Exemple**

Utilisation de la méthode tuple() pour créer un tuple :

```python
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets  
print(thistuple)
```

## Python - Accéder aux éléments Tuple

### Accéder aux éléments Tuple

Vous pouvez accéder aux éléments de tuple en vous référant au numéro d'index, entre crochets :

**Exemple**

Affichez le deuxième élément du tuple

```python
thistuple = ("apple", "banana", "cherry")  
print(thistuple[1])
```

> **Remarque** : Le premier élément a l'index 0.

### Indexation negative 

L'indexation negative signifie commencer par la fin.

-1 fait référence au dernier élément, -2 à l'avant-dernier élément, etc.

**Exemple**

Affichez le dernier élément du tuple

```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
```

### Plage d'index

Vous pouvez spécifier une plage d'index en spécifiant où commencer et où terminer la plage.

Lors de la spécification d'une plage, la valeur de retour sera un nouveau tuple avec les éléments spécifiés.

**Exemple**

Renvoie le troisième, quatrième et cinquième éléments :

```python
thistuple = ("apple", "banana", "cherry", "orange", "lemon", "melon", "mango")  
print(thistuple[2:5])
```

> **Remarque** : La recherche commencera à l'index 2 (inclus) et se terminera à l'index 5 (non inclus).

> N'oubliez pas que le premier élément a l'index 0.

En omettant la valeur de départ, la plage commencera au premier élément :

**Exemple**

Cet exemple renvoie les éléments du début à, mais NON inclus, "lemon":

```python
thistuple = ("apple", "banana", "cherry", "orange", "lemon", "melon", "mango")  
print(thistuple[:4])
```

En omettant la valeur de fin, la plage ira jusqu'à la fin de la liste :

**Exemple**

Cet exemple renvoie les éléments de "cerise" et jusqu'à la fin :

```python
thistuple = ("apple", "banana", "cherry", "orange", "lemon", "melon", "mango")  
print(thistuple[2:])
```

### Plage d'indices négatifs

Spécifiez des index négatifs si vous souhaitez commencer la recherche à partir de la fin du tuple :

**Exemple**

Cet exemple renvoie les éléments de l'index -4 (inclus) à l'index -1 (exclu)

```python
thistuple = ("apple", "banana", "cherry", "orange", "lemon", "melon", "mango")  
print(thistuple[-4:-1])
```

### Vérifier si l'élément existe

Pour déterminer si un élément spécifié est présent dans un tuple, utilisez le mot-clé `in` :

**Exemple**

Vérifiez si "apple" est présent dans le tuple :

```python
thistuple = ("apple", "banana", "cherry")  
if "apple" in thistuple:  
  print("Yes, 'apple' is in the fruits tuple")
```

## Python - Mettre à jour les tuples

Les **tuples** sont **immuables**, ce qui signifie que vous ne pouvez pas modifier, ajouter ou supprimer des éléments une fois le tuple créé.

Mais il existe des solutions de contournement.

### Modifier les valeurs de tuple

Une fois qu'un tuple est créé, vous ne pouvez pas modifier ses valeurs. Les tuples sont inchangeables, ou immuables comme on l'appelle aussi.

Mais il existe une solution de contournement. Vous pouvez convertir le tuple en une liste, modifier la liste et reconvertir la liste en un tuple.

**Exemple**

Convertissez le tuple en liste pour pouvoir le changer :

```python
x = ("apple", "banana", "cherry")  
y = list(x)  
y[1] = "kiwi"  
x = tuple(y)  
  
print(x)
```

### Ajouter des éléments

Puisque les tuples sont immuables, ils n'ont pas de méthode append() intégrée, mais il existe d'autres façons d'ajouter des éléments à un tuple.

1. **Convertir en liste** : Tout comme la solution de contournement pour modifier un tuple, vous pouvez le convertir en liste, ajouter vos éléments et le reconvertir en tuple.

**Exemple**
Convertissez le tuple en liste, ajoutez "orange" et reconvertissez-le en tuple :

```python
thistuple = ("apple", "banana", "cherry")  
y = list(thistuple)  
y.append("orange")  
thistuple = tuple(y)
```

2. **Ajouter un tuple à un tuple**. Vous êtes autorisé à ajouter des tuples aux tuples, donc si vous voulez ajouter un élément (ou plusieurs), créez un nouveau tuple avec le ou les éléments et ajoutez-le au tuple existant :

**Exemple**

Créez un nouveau tuple avec la valeur "orange", et ajoutez ce tuple :

```python
thistuple = ("apple", "banana", "cherry")  
y = ("orange",)  
thistuple += y  
  
print(thistuple)
```

> **Remarque** : lors de la création d'un tuple avec un seul élément, n'oubliez pas d'inclure une virgule après l'élément, sinon il ne sera pas identifié comme un tuple.

### Supprimer des éléments

> Remarque : Vous ne pouvez pas supprimer des éléments dans un tuple.

Les **tuples** ne sont pas modifiables, vous ne pouvez donc pas en supprimer des éléments, mais vous pouvez utiliser la même solution de contournement que celle que nous avons utilisée pour modifier et ajouter des éléments de tuple :

**Exemple**

Convertissez le tuple en liste, supprimez "apple" et reconvertissez-le en tuple :

```python
thistuple = ("apple", "banana", "cherry")  
y = list(thistuple)  
y.remove("apple")  
thistuple = tuple(y)
```

Ou vous pouvez supprimer complètement le tuple :

**Exemple**

Le mot-clé `del` peut supprimer complètement le tuple :

```python
thistuple = ("apple", "banana", "cherry")  
del thistuple  
print(thistuple) #this will raise an error because the tuple no longer exists
```

## Python - Loop Tuples

### Itérer sur un tuple

Vous pouvez parcourir les éléments du **tuple** en utilisant une boucle **for**.

**Exemple**

Parcourez les éléments et imprimez les valeurs :

```python
thistuple = ("apple", "banana", "cherry")  
for x in thistuple:  
  print(x)
```

### Itérer à travers les numéros d'index

Vous pouvez également parcourir les éléments du tuple en vous référant à leur numéro d'index.

Utilisez les fonctions `range()` et `len()` pour créer un itérable approprié.

**Exemple**

Imprimez tous les articles en vous référant à leur numéro d'index :

```python
thistuple = ("apple", "banana", "cherry")  
for i in range(len(thistuple)):  
  print(thistuple[i])
```

### Utilisation d'une boucle While

Vous pouvez parcourir les éléments du tuple en utilisant une **boucle while**.

Utilisez la fonction `len()` pour déterminer la longueur du tuple, puis commencez à 0 et parcourez les éléments du tuple en vous référant à leurs index.

N'oubliez pas d'augmenter l'indice de 1 après chaque itération.

**Exemple**

Imprimez tous les éléments, en utilisant une boucle while pour parcourir tous les numéros d'index :

```python
thistuple = ("apple", "banana", "cherry")  
i = 0  
while i < len(thistuple):  
  print(thistuple[i])  
  i = i + 1
```

[Next](./python_12_sets.md)