5 . Python: arguments
==========================


Si volem els arguments indicats a la línia de comandes, com per exemple:

```python
$ python hello.py Joan 
Hola, Joan.
```

podem fer-ho important el mòdul sys:

``` python
import sys
params = sys.argv # argv és una llista amb tots els arguments que passem
nom = params[1]
print ("Hola," nom)
```

> **Tasca:** Crea un script que realitzi càlculs senzills. El primer argument ha d'indicar el tipus de càlcul (_suma, resta_, etc.), i els següents els operadors de la operació.

