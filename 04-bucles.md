Python: bucles
==========================


**Veure la referència de [bucles a wikibooks](http://en.wikibooks.org/wiki/Python_Programming/Loops).**


Per fer un bucle típic numèric (no és el més habitual en Python):

``` python
for i in range(3,11,2):
   print (i)
```

Python itera a través de llistes d'objectes. La
instrucció `range(3,11,2)` crea una llista de nombres des de l'inici (3) fins el final (11) saltant de (2) en (2).



Dins dels bucles tenim unes clàusules que ens permeten major control:

-   `break`: finalitza i surt del bucle més proper.
-   `continue`: salta directament a la següent iteració del bucle.

Pots llegir aquí un [exemple de break i
continue](https://docs.python.org/3/tutorial/controlflow.html#break-and-continue-statements-and-else-clauses-on-loops).



> **Tasca:** Crea un programa que demani un número enter i en mostri la seva taula de multiplicar.

> **Tasca:** Millorar el programa de registre i login. En cas que es produeixi algun error, demanar a l'usuari que torni a entrar les dades tantes vegades com calgui.

