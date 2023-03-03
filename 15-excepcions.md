15 . Python: excepcions
==========================

A continuació es mostra com tractar excepcions:

```python
import sys

nom_fitxer= "fitxer.txt"
try:
    f = open(nom_fitxer, 'rb')
    data = f.read()
    f.close()
except IOError:
    # El flux d'execució arriba directament cap a aqui
    # si qualsevol de les línies anteriors llencen un IOError.
    sys.stderr.write('problema llegint: ' + nom_fitxer)
# En qualsevol cas, el codi continua després del try/except
```

> **Tasca:** Escriu un programa que faci divisions amb els números introduïts per l'usuari. En cas que es faci una divisió entre zero, capturar l'excepció i mostrar un missatge amigable a l'usuari.