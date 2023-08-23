# Python Get Started

## Installation

La plupart des PCs et Mac viennent avec Python déjà installé.
Pour savoir si vous avez python installé sur votre machine, exécutez la commande suivante:

```bash
john@ubuntu:~$python3 --version
```

Sous Windows

```bash
C:\Users\Your Name>python --version 
ou
C:\Users\Your Name>py --version
```

Si vous n'avez pas python installé sur votre machine, rendez-vous sur la page <a href="https://www.python.org/downloads/" target="_blank">python.org/downloads</a> pour télécharger l'exécutable.

Double cliquez sur le fichier téléchargé et suivez les instructions.

## Python Quickstart

Python est un langage de programmation interprété. Cela signifie qu'en tant que développeur, vous écrivez
des fichiers Python (.py) dans un éditeur de texte, puis vous placez ces fichiers dans l'interpréteur Python pour qu'ils soient exécutés.

La façon d'exécuter un fichier python est la suivante:

```bash
john@ubuntu:~$python3 helloworld.py
```

Sous Windows

```bash
C:\Users\Your Name>python helloworld.py
ou
C:\Users\Your Name>py helloworld.py
```

Où __helloworld.py__ est le nom de votre fichier python.

Écrivons notre premier fichier Python, appelé helloworld.py, qui peut être fait dans n'importe quel éditeur de texte.

```python
print("Hello world!")
```

Aussi simple que cela. Enregistrez votre fichier. Ouvrez votre terminal, accédez au répertoire dans lequel vous avez enregistré votre fichier et exécutez :

```bash
C:\Users\Your Name>python helloworld.py
```

La sortie doit indiquer : *Hello world!*

Vous pouvez également écrire du python dans votre terminal. Pour se faire, invoquez l'interpréteur python

```bash
C:\Users\Your Name>python
Python 3.10.6 (main, May 29 2023, 11:10:38) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello, World!")
```

Qui affichera "Hello, World!" dans la ligne de commande :

```bash
>>> print("Hello world!")
Hello world!
```

Chaque fois que vous avez terminé dans la ligne de commande python, vous pouvez simplement taper ce qui suit pour quitter l'interface de ligne de commande python :

```bash
>>>exit()
```

[Next →](./python_2_syntax.md)
