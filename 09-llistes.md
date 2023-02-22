7 . Python: llistes
=========================

Conceptes bàsics
----------------

Les llistes funcionen de manera similar als strings. Els literals s'escriuen entre corxets `[]`. El primer element es troba a l'índex 0.

```python
colors = ['vermell', 'verd', 'blau']
print(colors[0])
print(colors[2])
print(len(colors))  ## 3
```

```
               +-----------+--------+--------+
colors ------> | 'vermell' | 'verd' | 'blau' |
               +-----------+--------+--------+
           list      0          1        2
```

L'assignació amb `=` no realitza una còpia, sinò que les dues variables apunten a una única llista de la memòria:

```python
b = colors
```

```
               +-----------+--------+--------+
colors ------> | 'vermell' | 'verd' | 'blau' |
     b ------> +-----------+--------+--------+

```

La llista buida és un parell de corxets `[]`. El signe `+` permet "concatenar" dues llistes.

```python
llista_buida = []
print(llista_buida)

llista1 = [1, 2]
llista2 = [3, 4]
llista_combinada = llista1 + llista2
print(llista_combinada)
```



for & in
---------

La construcció `for ... in` és una forma senzilla de recòrrer cada element d'una llista. No afegir o eliminar cap element durant la iteració.

```python
quadrats = [1, 4, 9, 16]
sum = 0
for num in quadrats:
  sum += num
print(sum)  ## 30
```

Tenint en compte que a python no s'indiquen els tipus en la declaració de variables, és important escollir noms de es variables significatius.

La construcció `in` permet, de forma fàcil, saber si un element apareix a una llista (o un altre tipus de col·lecció).

```
llista = ['bart', 'lisa', 'marge']
if 'lisa' in llista:
  print('trobada!')
```

> **Tasca:** Escriu un programa que permeti a l'usuari introduïr una llista de pokemons. Quan l'usuari se'n cansi, mostrar la llista introduïda per pantalla.

Mètodes
-------

```python
llista = ['bart', 'lisa', 'marge']
print("1. ", llista)
llista.append('homer')         ## adjunta un element al final
print("2. ", llista)
llista.insert(0, 'xxx')        ## insereix un element a la posició indicada
print("3. ", llista)
llista.extend(['yyy', 'zzz'])  ## afegeix els elements al final
print("4. ", llista)
print("5. ", llista.index('lisa'))    ## retorna la posició de l'element indicat
llista.remove('lisa')         ## busca i elimina l'element
print("6. ", llista)
llista.reverse()              ## inverteix la llista
print("7. ", llista)
llista.pop(1)                  ## elimina i retorna l'element de la posició indicada
print("8. ", llista)
```

```
1.  ['bart', 'lisa', 'marge']
2.  ['bart', 'lisa', 'marge', 'homer']
3.  ['xxx', 'bart', 'lisa', 'marge', 'homer']
4.  ['xxx', 'bart', 'lisa', 'marge', 'homer', 'yyy', 'zzz']
5.  2
6.  ['xxx', 'bart', 'marge', 'homer', 'yyy', 'zzz']
7.  ['zzz', 'yyy', 'homer', 'marge', 'bart', 'xxx']
8.  ['zzz', 'homer', 'marge', 'bart', 'xxx']
```

> **Tasca:** Modifica el programa anterior per permetre a l'usuari "desfer" l'últim pokemon introduït.


Slices
------
La sintaxi _slice_ és una manera útil d'obtenir parts o seqüències. Funciona tant amb strings com amb llistes. El _slice_ `s[inici:final]` indica els elements començant per `inici` i finalitzant (sense incloure'l) a `final`.

```
 H  e  l  l  o
 0  1  2  3  4
-5 -4 -3 -2 -1
```

```python
s = "Hello"

print(s[1:4])
print(s[1:])
print(s[:]) # Útil per generar una còpia
print(s[1:100])
print()
print(s[-1])
print(s[-4])
print(s[:3])
print(s[-3:])
```

```
ell
ello
Hello
ello

o
e
Hel
llo
```

Veiem un exemple amb llistes:

```python
llista = ['a', 'b', 'c', 'd']
print(llista[1:-1])
llista[0:2] = 'z'    ## reemplaça ['a', 'b'] amb ['z']
print(llista)

enllaç = llista
copia = llista[:]
llista.reverse()
print(enllaç)
print(copia)
```

> **Tasca:** Partint de la idea dels pokemons, crea un CRUD de noms de pokemons.