Python: condicionals
==========================


## Blocs per indentació, ~~res de claus {}~~

Els blocs de sentències funcionen amb **indentació** (és a dir,
tabuladors/espais al principi de línia), el que és molt adequat per
establir un estil clar i net de programació.

``` python
a , b = 1, 2     # en Python podem fer assignacions de diverses variables alhora
if a == b:
   print("son iguals")
   c = True
else:
   print("son diferents")
   c = False
```

De pas, observa:
1. l'assignació múltiple
2. el condicional
3. els booleans son amb majúscula (True i False):

Cal tenir en compte que:

-   **Els inicis de bloc els marquen els dos punts ":"** de les
    sentències de control (condicionals, bucles) i de les funcions.
-   Tant ens fa posar un tabulador com 3 o 4 espais, la única regla és
    que **la indentació sigui coherent al llarg del bloc**.
-   Si estem copiant exemples de tutorials i similars, i després afegim
    codi, serà convenient ajustar el tipus d'indentació de l'editor per
    tal que sigui coherent. 

Condicionals
------------------
  
    
**Veure la referència de [condicionals a wikibooks](http://en.wikibooks.org/wiki/Python_Programming/Conditional_Statements).**

~~`switch`~~ no hi és en Python però al link anterior trobareu
    hàbils maneres de simular-ho.


Important remarcar
que els condicionals es poden fer de la manera curta amb:

``` python
num = int(input())
res = -num if num<0 else num
print(res)
```

Fixa't que hem filtrat l'entrada per tal que `num` sigui un sencer (`int`). Si volguéssim un flotant caldria fer:

```python
num = float(input())
```


> **Tasca:** Fes un programa que executi:
- Una pantalla de registre. Ha de demanar el nom d'usuari i dues vegades la contrasenya. Si no coincideix mostrar un error.
- Una pantalla de login. Ha de demanar el nom d'usuari i la contrasenya. Si no coincideix amb els entrats a l'inici mostrar un error.