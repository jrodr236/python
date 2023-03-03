16 . Python: classes
==========================

Classe i instància
------------------

- Una classe defineix un tipus.
- Una instància és un objecte concret creat a partir del model d'una classe.
- Els atributs (variables internes) els creem inicialitzant-los a un valor.
- Els mètodes (funcions internes) es creen amb def i TOTES tenen com a primer argument self (= la instància que el crida).

Aquest exemple mostra una classe amb atributs:

```python
class Persona:
  def __init__(self, nom, edat):
    self.nom = nom
    self.edat = edat

p1 = Persona("Joan", 36)

print(p1.nom)
print(p1.edat)
```

El següent és una classe amb atributs i mètodes.

```python
class Pilota:
  def __init__(self, posx, posy, velocitat):
    # atributs
    self.velocitat = velocitat
    self.posx = posx
    self.posy = posy
  # mètodes
  def accelera(self):
    self.velocitat = self.velocitat + 5
  def canviarPosicio(self, x, y):
    self.posx = x
    self.posy = y


p = Pilota(3, 5, 10)
print(p.velocitat)
print(p.posy)

p.posy = 8
print(p.posy)

p.accelera()
print(p.velocitat)
p.canviarPosicio(40,30)
print(p.posx)
print(p.posy)
```

Visibilitat
-----------
A Python tots els atributs i mètodes son públics. Es pot "marcar" com a privat un atribut si el comencem amb un underscore, per exemple:

```python
class Bicicleta():
   _velocitat = 0
   def accelera(self):
      self._velocitat = self.velocitat + 5
```

El fet de posar el underscore no afecta a la visibilitat, però és una "convenció" de que si trobem un atribut d'aquest tipus, no convé accedir-hi directament.

> **Tasca:** Dissenya una classe per als pokemons, amb el seu nom i unes poques característiques principals. Crea'n dos instàncies.