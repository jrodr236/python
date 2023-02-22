11 . Python: slice
=========================

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

> **Tasca:** Fes _slice_ sobre l'string `Toscana` per obtenir: `"Tosc"`, `"cana"`, `"can"`.

> **Tasca:** Fes _slice_ sobre 
>
>>"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
>
> per obtenir `laborum` (sense el punt final).

> **Tasca:** Fes _slice_ sobre la llista `[40,50,20,30,90]`  perquè mostri: `[30,90]`, `[50, 20]` 

