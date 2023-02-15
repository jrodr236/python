Python: exercicis bàsics
==========================

Calculadora Freelancer
----------------------
Un Freelancer desitja saber quant pot cobrar per la seva feina setmanalment i mensualment. Per això només necessita establir el preu de la seva feina per hora.

S'estimen 40 hores de feina a la setmana.

Les fórmules per calcular el pagament Setmanal i Mensual són:

1) Pagament_Semanal = (EurosPerHora x 40)
2) Pagament_Mensual = (EurosPerHora x 160)

El programa haurà de demanar el preu per hora i mostrarà el resultat del pagament setmanal i el mensual.

Per exemple:
```
Preu en euros por hora: 20

Pagament setmanal: 800.00
Pagament mensual: 3200.00
```

Edat de 2 persones
-----------------

Escriu un programa que demani l'edat de 2 persones i digui si és major la primera, la segona, o si tenen la mateixa edat.


Signe del zodíac
----------------

Fes un script que demani nom, cognom, lloc i data de naixement, i
    mostri per pantalla les dades personals formatades dins d'una frase
    més el signe del zodíac de la persona.

Per exemple, la sortida podria ser:
```
Sr./Sra. Josep Pérez, nascut a Andorra l'any 1991, té a Taure com a signe solar del zodíac.
```

Podeu utilitzar la [llibreria python datetime](https://docs.python.org/3/library/datetime.html#datetime-objects).


Interès anual
--------------

Escriu un programa que pregunti a l'usuari una quantitat a invertir, l'interès anual i el nombre d'anys, i mostri per pantalla el capital obtingut a la inversió cada any que dura la inversió.

Per exemple:
```
Quantitat a invertir? 1000
Interès percentual anual? 10
Anys? 5

Capital després de 1 anys: 1100.0
Capital després de 2 anys: 1210.0
Capital després de 3 anys: 1331.0
Capital després de 4 anys: 1464.1
Capital després de 5 anys: 1610.51
```