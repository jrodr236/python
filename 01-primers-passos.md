1 . Python: primers passos
===========================

## Importància de python

[Google: programing languages ranking](https://www.google.com/search?q=programing+languages+ranking)

## A Windows

Descarregar i instal·lar [Python](https://www.python.org/downloads/).
- Escollir _Add python.exe to PATH_.
- Escollir _Disable max path limit_.

## A Linux

Acostuma a estar instal·lat.


## Consola

Python és un llenguatge interpretat i es pot invocar la consola des de l'entorn de comandes:

```python
> python
Python 3.11.1 (tags/v3.11.1:a7a450f, Dec  6 2022, 19:58:39) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> a=1
>>> print(a)
1
```

Per sortir feu servir quit() o CTRL+z (CTRL+d a Linux).

> **Tasca:** Executa el codi anterior a la consola de python.


## Script

Volem executar un script de python:
```python
#!/usr/bin/env python3

print('Hello world!')
```

```bash
$ python elmeuscript.py
```


A Linux, a més, es pot executar directament

```bash
$ chmod 755 elmeuscript.py
$ ./elmeuscript.py
```

> **Tasca:** Crea i executa un script que mostri el teu nom per pantalla.


## Accents i demés: codificació UTF-8 de l'arxiu

Si teniu problemes amb les cadenes de caràcters en el nostre idioma, cal especificar al principi de l'arxiu que treballem amb la codificació UTF-8:

``` python
#!/usr/bin/python
# -*- coding: utf-8 -*-
print "mira què bé"
```

## IDE

* Per a projectes professionals (CFGS DAM), recomanem l'ús de l'IDE [PyCharm Professional](https://www.jetbrains.com/pycharm/).

* Per a introduïr-se a Python (CFGM SMX), recomanem l'ús de l'IDE [Thonny](https://thonny.org/). Aquest IDE està instal·lat per defecte a Raspberry Pi.


> **Tasca:** Des de l'IDE, executa un programa que mostri un acudit per pantalla.

