17 . Python: lambda
==========================

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