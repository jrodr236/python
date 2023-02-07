Python: strings
==========================

  
## Formatació de strings (cadenes de caràcters)

Per imprimir variables dins d'una cadena de caràcters es pot fer de
diverses maneres. La primera seria concatenant amb "+":

``` python
nom = "Manolo"
missatge = "El guanyador del premi és " + nom + ". Felicitats!"
```

La segona seria intercal·lant les variables entre comes (`,`):

``` python
nom = input("Digues el teu nom: ")
edat = input ("Digues la teva edat: ")
print ("Hola", nom, ", tens", edat, "anys.")
```

> **Tasca opcional:** Soluciona el problema amb l'espai abans de la coma (`,`) de l'últim exemple.

La tercera seria intercal·lant les variables amb %, similar al C, i posant els arguments entre parèntesi (és una tupla, ho veurem més tard) després d'un "%":

```python
nom = "Joan"
edat = 43
print("Hola %s, tens %d anys." % (nom, edat))
```

Els principals valors que pot prendre son:

- %s: string
- %d: decimal (sencer)
- %f: float (punt flotant, nombres reals).

Per controlar el nº de decimals podem posar el modificador `<nombre_de_decimals>` entre el `%` i la `f`. Per exemple:

```python
pi = 3.14159
print("pi = %.3f" % pi)
```
Imprimeix només 3 decimals (al tanto que arrodoneix!):
```
pi = 3.142
```


## Més coses de strings

Per omplir (padding) un string es pot fer:

```python
>>> a = "p" * 5
>>> a
'ppppp'
```

Per separar un string en parts ho podem fer amb `split` (equival al
`explode` del PHP):

```python
>>> a = 'xxxx.xxxx.abcd'
>>> a.split(".")
['xxxx', 'xxxx', 'abcd']
```

Per transformar a majúscules o minúscules:

``` python
>>> a = "cOsES"
>>> a.upper()
'COSES'
>>> a.lower()
'coses'
```

La llibreria string té coses interessants:

``` python
>>> import string
>>> string.ascii_uppercase
'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
>>> string.ascii_lowercase
'abcdefghijklmnopqrstuvwxyz'
```

Per saber més prova amb `dir(str)` o mira aquí:

-   http://docs.python.org/library/string.html
-   https://docs.python.org/library/stdtypes.html#string-methods
-   http://docs.python.org/tutorial/inputoutput.html

  

> **Tasca:** Implementa un programa que, a partir del nom, cognom i any de naixement de l'usuari, recomani noms d'usuari per aquella persona. Per exemple:
> - nom.cognom
> - inicial+cognom
> - cognom+any_naixement
> - cognom invertint les lletres
> - un parell més que se t'acudeixin