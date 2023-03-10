12 . Python: tuples
=========================

Una tupla és una agrupació d'elements de mida fixa. Son semblant als `struct` d'altres llenguatges de programació. Al contrari que les llistes, les tuples son constants, no es poden modificar després de crear-les.

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

> **Tasca:** Crea una funció que rebi una tupla per paràmetre amb una data (dia, més i any). La funció ha de retornar una tupla amb el dia següent.
>
> **Tasca:** Busca a Internet i respón: en quins casos és millor utilitzar tuples enlloc de llistes i quines avantatges té?