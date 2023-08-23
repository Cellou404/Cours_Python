# Python - Booleans

Les booléens représentent l'une des deux valeurs suivantes : True (Vrai) ou False (Faux).

## Valeurs booléennes
En programmation, vous avez souvent besoin de savoir si une expression est vraie ou fausse.

Vous pouvez évaluer n'importe quelle expression en Python et obtenir l'une des deux réponses, Vrai ou Faux.

Lorsque vous comparez deux valeurs, l'expression est évaluée et Python renvoie la réponse booléenne :

**Exemple**

```python
print(10 > 9)
print(10 == 9)
print(10 < 9)
```

Lorsque vous exécutez une condition dans une instruction if, Python renvoie True ou False :

**Exemple**

Afficher un message selon que la condition est vraie ou fausse :

```python
a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

## Évaluer les valeurs et les variables

La fonction bool() vous permet d'évaluer n'importe quelle valeur, et de vous donner Vrai ou Faux en retour,

**Exemple**
Evaluer une chaîne et un nombre :

```python
print(bool("Hello"))
print(bool(15))
```

**Exemple**

Evaluer deux variables:

```python
x = "Hello"
y = 15

print(bool(x))
print(bool(y))
```

## La plupart des valeurs sont vraies

Presque toutes les valeurs sont évaluées à True si elles ont une sorte de contenu.

Toute chaîne est vraie, à l'exception des chaînes vides.

Tout nombre est vrai, sauf 0.

Toutes les listes, tuples, ensembles et dictionnaires sont vrais, sauf ceux qui sont vides.

**Exemple**

Ce qui suit renverra True :

```python
bool("abc")
bool(123)
bool(["apple", "cherry", "banana"])
```

## Certaines valeurs sont fausses

En fait, il n'y a pas beaucoup de valeurs évaluées à False, à l'exception des valeurs vides, telles que (), [], {}, "", le nombre 0 et la valeur None. Et bien sûr, la valeur False est évaluée à False.

**Exemple**

Ce qui suit renverra False :

```python
bool(False)
bool(None)
bool(0)
bool("")
bool(())
bool([])
bool({})
```

## Les fonctions peuvent renvoyer un booléen

Vous pouvez créer des fonctions qui renvoient une valeur booléenne :

**Exemple**

Imprimer la réponse d'une fonction :

```python
def myFunction() :
  return True

print(myFunction())
```

Vous pouvez exécuter du code basé sur la réponse booléenne d'une fonction :

**Exemple**

Imprimer "OUI !" si la fonction renvoie True, sinon imprimez "NO!" :

```python
def myFunction() :
  return True

if myFunction():
  print("YES!")
else:
  print("NO!")
```

[Next](./python_9_operators.md)
