Python: gestió de dades, introducció
======================


## Variables dinàmiques

En Python, igual que en molts llenguatges interpretats, no cal declarar el tipus de les variables. Es pot crear una variable quan es vulgui i del tipus que es vulgui i es pot canviar al llarg de l'execució. Per
exemple:

``` python
>>> a = 1
>>> type(a), a
(<class 'int'>, 1)
>>> a = "cosa"
>>> type(a), a
(<class 'str'>, 'cosa')
```


## Entrada de dades per teclat

```python
>>> xx = input()  
hola
>>> xx 
'hola'
```

## Per entrar contrassenyes

Podem importar una funció "getpass" del mòdul del mateix nom,
per entrar passwords sense que es mostri per pantalla:

``` python
import getpass
password = getpass.getpass("Entra la teva contrassenya: ")
```


> **Tasca:** Crea una pantalla de login. Per verificar les dades, fes que mostri l'usuari i la contrasenya en finalitzar.

