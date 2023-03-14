17 . Python: lambda
==========================

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

Veiem un altre exemple, en aquest cas amb la funció `filter()`, que permet _filtrar_ els valors d'una llista:

```python
numeros = [-12, 65, 54, 39, -102, -339, 221, -50, 70, ]
numeros_positius = list(filter(lambda x: (x > 0), numeros))
print(numeros_positius)
```

> **Tasca:** Utilitzant funcions lambda i filter(), escriu una funció que retorni només els números parells d'una llista d'enters.

Lambda i objectes
-----------------
Les funcions lambda també son molt útils en cas de treballar amb objectes.

```python
class Persona:
    def __init__(self, nom, ciutat_de_naixement, any_de_naixement):
        self._nom = nom
        self._ciutat_de_naixement = ciutat_de_naixement
        self._any_de_naixement = any_de_naixement

    def get_nom(self):
        return self._nom

    def get_ciutat_de_naixement(self):
        return self._ciutat_de_naixement

    def get_any_de_naixement(self):
        return self.get_any_de_naixement

    def __str__(self):
        return self._nom + ", nascut a " + self._ciutat_de_naixement + " l'any " + self._any_de_naixement + "."


abril = Persona("Abril", "Barcelona", "1968")
josep = Persona("Josep", "Andorra", "2001")
marta = Persona("Marta", "Olot", "1999")

llista_de_persones = [abril, josep, marta]

print("Ordre original")
for persona in llista_de_persones:
    print(persona)
print()

# print("Ordre per defecte")
# for persona in sorted(llista_de_persones):
#     print(persona)
# print()
# Retorna l'error:
# TypeError: '<' not supported between instances of 'Persona' and 'Persona'

print("Ordre per nom")
for persona in sorted(llista_de_persones, key=lambda x: x.get_nom()):
    print(persona)
print()
```

Fixa't en alguns detalls de la classe:
- Té atributs marcats com a _privats_ i s'han creat mètodes `get` per accedir-hi.
- S'ha implementat el mètode `__str__()`, que és equivalent al `toString()` de java. És a dir, retorna la representació com a `String` de l'objecte quan és necessari.

> **Tasca:** Modifica l'exemple perquè les persones s'ordenin per edat.