12 . Python: tuples
=========================

Una tupla és una agrupació d'elements de mida fixa. Son semblant als `struct` d'altres llenguatges de programació.

```python
tupla = (1, 2, 'hola')
print(len(tupla))
print(tupla[2])
# tupla[2] = 'bye'  ## NO, tuples cannot be changed
tupla = (1, 2, 'adeu')
```

Per diferenciar una tupla d'un sol element de una expressió sense parèntesis, s'hi ha d'afegir una coma:

```python
tupla = ('hola',)
```

Podem assignar una tupla a una altra de la mateixa mida:

```python
(a, b, c) = (42, 13, "super!")
```

> **Tasca:** Estem en un equip de programació encarregat de desenvolupar un joc electrònic basat en el [Whac-A-Mole](https://ca.wikipedia.org/wiki/Whac-A-Mole_(videojoc)). Els talps poden sortir en una de les posicions d'un rectangle de 3x3. Crea una funció que retorni una tupla amb la posició aleatòria a on apareixeria el talp.