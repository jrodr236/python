7 . Python: funcions
==========================

Les funcions a Python es defineixen de la següent forma:

```python
# Defineix la funció "repetir" que rep 2 arguments.
def repetir(s, exclamar):
    """
    Retorna l'string 's' repetit 3 vegades.
    Si exclamar és true, afegir signes d'exclamació.
    """

    resultat = s + s + s # també es pot fer servir "s * 3", que és més ràpid (Perquè?)
    if exclamar:
        resultat = resultat + '!!!'
    return resultat
```

La paraula clau `def` defineix la funció amb els seus paràmetres entre parèntesis i el seu codi amb indentació.

A continuació es mostra el codi que cridaria a la funció `repetir`:

```python
def main():
    print(repetir('Yay', False))      ## YayYayYay
    print(repetir('Woo Hoo', True))   ## Woo HooWoo HooWoo Hoo!!!

# Codi estàndard per cridar la funció main() per començar
# el programa.
if __name__ == '__main__':
    main()
```

Aprofitem per explicar que els arxius de codi de Python utilitzen l'extensió `.py` i s'anomenen "mòduls".

Un mòdul de Python es pot executar directament (com `python hola.py Joan`) o es poden importar i utilitzar. Quan s'executa directament un arxiu de Python, la variable especial `__name__` s'estableix com a `__main__`. Per tant, és comú tenir el codi estàndard `if __name__ == ...` anterior per a cridar a una funció `main()` quan el mòdul s'executa directament, però no quan un altre mòdul l'importa.

> **Tasca:** Escriu tres funcions que retornin, cadascuna, si un DNI és vàlid, si una data és vàlida i si una adreça de correu és vàlida. Utilitzant la forma estàndard per cridar a la funció `main()`, escriu un programa que demani a l'usuari les seves dades personals i les validi utilitzant les funcions anteriors.