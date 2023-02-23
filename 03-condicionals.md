3 . Python: condicionals
==========================


## Blocs per indentació, ~~res de claus {}~~

Els blocs de sentències funcionen amb **indentació** (és a dir,
tabuladors/espais al principi de línia), el que és molt adequat per
establir un estil clar i net de programació.

``` python
a, b = 1, 2     # a Python podem fer assignacions de diverses variables alhora
if a == b:
   print("son iguals")
   c = True
else:
   print("son diferents")
   c = False
print(c)
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

Les instruccions condicionals permeten que el programa executi o no unes sentències en funció d'una condició.

```python
entrada = input("Enter? ") # Demana un enter.
entrada = int(entrada) # Defineix entrada com l'enter escollit.
if entrada < 0:
    resultat = -entrada
else:
    resultat = entrada
print ("El valor absolut de ", entrada, "és", resultat)
```


Important remarcar
que els condicionals es poden fer de la manera curta amb:

``` python
entrada = int(input("Enter? "))
resultat = -entrada if entrada<0 else entrada
print ("El valor absolut de ", entrada, "és", resultat)
```

Fixa't que hem filtrat l'entrada per tal que `num` sigui un sencer (`int`). Si volguéssim un flotant caldria fer:

```python
entrada = float(input())
```

Ara veiem la instrucció elif (s'explicarà el `while` més endavant):

```python
a = 0
while a <= 10:
    if a > 5:
        print (a,">",5)
    elif a <= 7:
        print (a,"<=",7)
    else:
        print ("Cal dels anteriors és cert")
    a = a + 1
```

Fixa't en la sortida:

```
0 <= 7
1 <= 7
2 <= 7
3 <= 7
4 <= 7
5 <= 7
6 > 5
7 > 5
8 > 5
9 > 5
10 > 5
```

Què passaria si canviem el `elif` per un `if`?




~~`switch`~~ no hi és en Python però al link següent trobareu
    hàbils maneres de simular-ho.

Per més informació, veure la referència de [condicionals a wikibooks](http://en.wikibooks.org/wiki/Python_Programming/Conditional_Statements).

> **Tasca:** Fes un programa que executi:
> - Una pantalla de registre. Ha de demanar el nom d'usuari i dues vegades la contrasenya. Si no coincideix mostrar un error.
> - Una pantalla de login. Ha de demanar el nom d'usuari i la contrasenya. Si no coincideix amb els entrats a l'inici mostrar un error.