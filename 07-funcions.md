7 . Python: funcions
==========================

Definició i crida
-----------------

Les funcions a Python es defineixen de la següent forma:

```python
# Defineix la funció "repetir" que rep 2 arguments.
def repetir(s, exclamar):
    """
    Retorna l'string 's' repetit 3 vegades.
    Si exclamar és true, afegir signes d'exclamació.
    """

    resultat = s + s + s # també es pot fer servir "s * 3", que és més ràpid (Perquè?)
    if exclamar:
        resultat = resultat + '!!!'
    return resultat
```

La paraula clau `def` defineix la funció amb els seus paràmetres entre parèntesis i el seu codi amb indentació.

A continuació es mostra el codi que cridaria a la funció `repetir`:

```python
def main():
    print(repetir('Yay', False))      ## YayYayYay
    print(repetir('Woo Hoo', True))   ## Woo HooWoo HooWoo Hoo!!!

# Codi estàndard per cridar la funció main() per començar
# el programa.
if __name__ == '__main__':
    main()
```

Aprofitem per explicar que els arxius de codi de Python utilitzen l'extensió `.py` i s'anomenen "mòduls".

Un mòdul de Python es pot executar directament (com `python hola.py Joan`) o es poden importar i utilitzar. Quan s'executa directament un arxiu de Python, la variable especial `__name__` s'estableix com a `__main__`. Per tant, és comú tenir el codi estàndard `if __name__ == ...` anterior per a cridar a una funció `main()` quan el mòdul s'executa directament, però no quan un altre mòdul l'importa.



> **Tasca:** Escriu tres funcions que retornin, cadascuna, si un DNI és vàlid, si una data és vàlida i si una adreça de correu és vàlida. Utilitzant la forma estàndard per cridar a la funció `main()`, escriu un programa que demani a l'usuari les seves dades personals i les validi utilitzant les funcions anteriors.


Paràmetres opcionals i amb nom
------------------------------

A Python és possible assignar valors per defecte als paràmetres de les funcions. Això significa que aquests paràmetres es converteixen en opcionals. A més, podem cridar a la funció utilitzant els noms dels paràmetres.

```python
def saludar(nom, missatge='Hola'):
    print(missatge, nom)

saludar('John Smith')
saludar(missatge="Bon dia", nom="Rigoberta")
```

Funcions lambda
---------------
Una funció lambda és una petita funció anònima. Pot genir varis arguments, però només una expressió.

```python
x = lambda a : a + 10
print(x(5))

x = lambda a, b : a * b
print(x(5, 6))

x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```

Les funcions lambda son útils per utilitzar-les com a paràmetre d'altres funcions:

```python
paraules = ("hola", "que", "tal", "estas")
paraules_ordenades_alfabeticament = sorted(paraules) # per defecte, ordena alfabèticament
print(paraules_ordenades_alfabeticament)
paraules_ordenades_per_longitud = sorted(paraules, key=lambda x: len(x)) # ordena per la longitud
print(paraules_ordenades_per_longitud)
```

> **Tasca:** Utilitzant funcions lambda i filter(), escriu una funció que retorni només els valors positius d'una llista d'enters.