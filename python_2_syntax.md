# Python Syntax

## Exécuter la syntaxe Python

Comme nous l'avons appris précédemment, la syntaxe Python peut être exécutée en écrivant directement dans la ligne de commande :

```shell
>>> print("Hello, World!")
Hello, World!
```

Ou en créant un fichier python sur le serveur, en utilisant l'extension de fichier __.py__ et en l'exécutant dans la ligne de commande :

```bash
C:\Users\Your Name>python myfile.py
```

## Indentation Python

L'indentation fait référence aux espaces au début d'une ligne de code.

Alors que dans d'autres langages de programmation, l'indentation dans le code sert uniquement à la lisibilité, l'indentation dans Python est très importante.

Python utilise l'indentation pour indiquer un bloc de code.

```python
if 5 > 2:
  print("Cinq est plus grand que deux!")
```

Python vous renverra une erreur si vous ignorez l'indentation (IndentationError) :

```python
if 5 > 2:
print("Cinq est plus grand que deux!")
```

Le nombre d'espaces dépend de vous en tant que programmeur, l'utilisation la plus courante est de quatre, mais il doit y en avoir au moins un.

```python
if 5 > 2:
  print("Cinq est plus grand que deux!")
if 5 > 2:
 print("Cinq est plus grand que deux!")
```

Vous devez utiliser le même nombre d'espaces dans le même bloc de code, sinon Python vous donnera une erreur :

```python
if 5 > 2:
  print("Cinq est plus grand que deux!")
   print("Biensûre, Cinq est plus grand que deux!")
```

[Next →](./python_3_comments.md)
