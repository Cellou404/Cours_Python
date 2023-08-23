# Python - Les variables

## Les Variables

### Définition

Les variables sont des conteneurs pour stocker des valeurs de données.

### Création de variables

Python n'a pas de commande pour déclarer une variable.

Une variable est créée au moment où vous lui attribuez une valeur pour la première fois.

```python
x = 5
y = "John"
print(x)
print(y)
```

Les variables n'ont pas besoin d'être déclarées avec un type particulier et peuvent même changer de type après avoir été définies.

```python
x = 10       # x est de  type int
x = "Je suis de type str"  # x est de type str
print(x)
```

### Casting

Si vous souhaitez spécifier le type de données d'une variable, vous pouvez le faire avec la méthode cast.

```python
x = str(3)    # x sera '3'
y = int(3)    # y sera 3
z = float(3)  # z sera 3.0
```

### Obtenez le type

Vous pouvez obtenir le type de données d'une variable avec la fonction type().

```python
x = 5
y = "John"
print(type(x))
print(type(y))
```

Vous en apprendrez plus sur les types de données et le casting plus loin dans ce didacticiel.

### Guillemets simples ou doubles ?

Les variables de type chaîne peuvent être déclarées en utilisant des guillemets simples ou doubles :

```python
x = "John"
# est le même que
x = 'John'
```

### Case-Sensitive (Sensible aux majuscules et minuscules)

Les noms de variables sont sensibles à la casse.

```python
a = 4
A = "Sally"
#A n'écrasera pas a
```

## python - Noms des variables

### Noms des variables

Une variable peut avoir un nom court (comme x et y) ou un nom plus descriptif (age, carname, total_volume). Règles pour les variables Python :

- Un nom de variable doit commencer par une lettre ou le caractère de soulignement
- Un nom de variable ne peut pas commencer par un chiffre
- Un nom de variable ne peut contenir que des caractères alphanumériques et des traits de soulignement (A-z, 0-9 et _ )
- Les noms de variables sont sensibles à la casse (age, Age et AGE sont trois variables différentes)
- Un nom de variable ne peut pas être l'un des mots-clés Python.

#### Exemple 1

Noms des variables légales:

```python
myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"
```

#### Exemple 2

Noms de variables illégales:

```python
2myvar = "John"
my-var = "John"
my var = "John"
```

**NB:** N'oubliez pas que les noms de variables sont sensibles à la casse.

### Noms de variables multi-mots

Les noms de variable avec plus d'un mot peuvent être difficiles à lire.

Il existe plusieurs techniques que vous pouvez utiliser pour les rendre plus lisibles :

#### Camel Case

Chaque mot, sauf le premier, commence par une majuscule :

```python
myVariableName = "John"
```

#### Pascal Case

Chaque mot commence par une lettre majuscule:

```python
MyVariableNome = "John"
```

#### Snake Case

Chaque mot est séparé par un trait de soulignement(underscore) :

```python
my_variable_name = "John"
```

## Variables Python - Attribuer plusieurs valeurs

### De nombreuses valeurs à plusieurs variables

Python vous permet d'attribuer des valeurs à plusieurs variables sur une seule ligne :

```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

**Remarque** : Assurez-vous que le nombre de variables correspond au nombre de valeurs, sinon vous obtiendrez une erreur.

### Une valeur à plusieurs variables

Et vous pouvez attribuer la même valeur à plusieurs variables sur une seule ligne :

```python
x = y = z = "Orange"
print(x)
print(y)
print(z)
```

### Déballer une collection

Si vous avez une collection de valeurs dans une liste, un tuple, etc. Python vous permet d'extraire les valeurs dans des variables. C'est ce qu'on appelle le déballage (unpacking).

#### Exemple

Décompressez une liste :

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```

On apprendra plus sur la decompression des tuples en un chapitre ulterieur.

## Python - Variables de sortie

### Variables de sortie

La fonction Python print() est souvent utilisée pour sortir des variables.

```python
x = "Python is awesome"
print(x)
```

Dans la fonction print(), vous pouvez afficher plusieurs variables, séparées par une virgule :

```python
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)
```

Remarquez le caractère espace après "Python " et "is", sans eux le résultat serait "Pythonisawesome".

Pour les nombres, le caractère __+__ fonctionne comme un opérateur mathématique :

```python
x = 5
y = 10
print(x + y)
```

Dans la fonction print(), lorsque vous essayez de combiner une chaîne et un nombre avec l'opérateur +, Python vous renvoie une erreur :

```python
x = 5
y = "John"
print(x + y)
```

La meilleure façon de générer plusieurs variables dans la fonction print() consiste à les séparer par des virgules, qui prennent même en charge différents types de données :

```python
x = 5
y = "John"
print(x, y)
```

## Python - Variables globales

### Les Variables globales
Les variables créées en dehors d'une fonction (comme dans tous les exemples ci-dessus) sont appelées variables globales.

Les variables globales peuvent être utilisées par tout le monde, à la fois à l'intérieur des fonctions et à l'extérieur.

#### Exemple 1
Créer une variable en dehors d'une fonction et l'utiliser à l'intérieur de la fonction

```python
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

Si vous créez une variable avec le même nom dans une fonction, cette variable sera locale et ne pourra être utilisée qu'à l'intérieur de la fonction. La variable globale portant le même nom restera telle quelle, globale et avec la valeur d'origine.

#### Exemple 2
Créer une variable à l'intérieur d'une fonction, avec le même nom que la variable globale

```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
```

### Le mot-clé global

Normalement, lorsque vous créez une variable dans une fonction, cette variable est locale et ne peut être utilisée qu'à l'intérieur de cette fonction.

Pour créer une variable __globale__ dans une fonction, vous pouvez utiliser le mot clé __global__.

#### Exemple 1
Si vous utilisez le mot-clé __global__, la variable appartient à la portée globale :

```python
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

Utilisez également le mot-clé __global__ si vous souhaitez modifier une variable globale dans une fonction.

#### Exemple 2
Pour modifier la valeur d'une variable globale à l'intérieur d'une fonction, faites référence à la variable en utilisant le mot-clé global :

```python
x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

[Next ⟶](./python_5_data_type.md)