```python
import time

def potenciaIterativa(b, n):
    resultat = 1
    while n >= 1:
        resultat = resultat * b
        n = n - 1
    return resultat

def potenciaRecursiva1(b, n):
    if n <= 0:
        return 1
    else:
        return b * potenciaRecursiva1(b, n-1)

def potenciaRecursiva2(b, n):
    """ Precondició: n ha de ser més gran o igual que zero.
        Retorna: b\^n. """

    # Cas base
    if n <= 0:
        return 1

    # n parell
    if n % 2 == 0:
        pot = potenciaRecursiva2(b, n / 2)
        return pot * pot
    # n senar
    else:
        pot = potenciaRecursiva2(b, (n - 1) / 2)
        return pot * pot * b

base = int(input("Base? "))
exponent = int(input("Exponent? "))

ns_inici = time.perf_counter_ns()
print(potenciaIterativa(base, exponent))
ns_iterativa = time.perf_counter_ns()
print(potenciaRecursiva1(base, exponent))
ns_recursiva1 = time.perf_counter_ns()
print(potenciaRecursiva2(base, exponent))
ns_recursiva2 = time.perf_counter_ns()
print(ns_iterativa - ns_inici)
print(ns_recursiva1 - ns_iterativa)
print(ns_recursiva2 - ns_recursiva1)
```