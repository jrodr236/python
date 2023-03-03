13 . Python: diccionaris
=========================

Ús bàsic
--------

Els diccionaris son estructures que permeten emmagatzemar parelles de clau:valor. Les claus poden ser Strings, números i tuples. El tipus de les claus pot ser qualsevol.

```
+-----------+
|   claus   |      valors
| +-------+ |   +---------+
| |  'a'  |-+-->| 'alpha' |
| +-------+ |   +---------+
|           |
| +-------+ |   +---------+
| |  'o'  |-+-->| 'omega' |
| +-------+ |   +---------+
|           |
| +-------+ |   +---------+
| |  'g'  |-+-->| 'gamma' |
| +-------+ |   +---------+
|           |
+-----------+
```

```python
dict = {}
dict['a'] = 'alpha'
dict['g'] = 'gamma'
dict['o'] = 'omega'

print(dict)
print(dict['a'])
dict['a'] = 6
print(dict)
print('a' in dict)
## print(dict['z'])                  ## Llança una excepció KeyError
if 'z' in dict: print(dict['z'])  ## Evita el KeyError
print(dict.get('z'))
```

Recorreguts
-----------
Per defecte, un bucle sobre un diccionari recorre les seves claus, en un ordre arbitrari. També hi han els mètodes `dict.keys()` i `dict.values()` que retornen les claus i els valors. El mètode `items()` retorna una llista de tuples (clau, valor), que és la forma més eficient d'examinar totes les claus i valors del diccionari. Totes aquestes llistes permeten utilitzar la funció `sorted()` per ordenar-les.

```python
dict = {
    'a': 'alpha',
    'o': 'omega',
    'g': 'gamma'
}

for key in dict: print(key)         # Mostra les claus, una a una
print()
for key in dict.keys(): print(key)  # El mateix que l'anterior
print()
print(dict.keys())                  # Mostra les claus
print()
print(dict.values())                # Mostra els valors
print()
for key in sorted(dict.keys()):     # Mostra les parelles clau:valor, una a una, ordenant les claus
    print(key, dict[key])
print()
print(dict.items())                 # Mostra parelles (clau, valor)
print()
for k, v in dict.items(): print(k, '>', v) # L'accés es realitza sobre una llista de tuples
```


> **Tasca:** Crea un programa amb 2 funcionalitats:
> - Primer, demanarà noms de pokemons i el seu tipus.
> ![tipus de pokemons](https://easycdn.es/1/imagenes/pokemaster_343217_pn2.jpg)
> - Després, l'usuari podrà indicar un nom de pokemon i el programa retornarà quin és el seu tipus.

