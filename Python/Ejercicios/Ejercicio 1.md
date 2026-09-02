Con lo visto en [[1. Introducción]], [[2. Tipos de datos]] y [[3. Control de flujo]] resolver:
## 🧪 Ejercicio 1 — Clasificador de números

Escribí un programa que le pida al usuario **10 números enteros**, uno por uno, y al finalizar informe:

1. Cuántos números fueron **positivos**.
2. Cuántos fueron **negativos**.
3. Cuántos fueron **cero**.
4. La **suma total** de todos los números ingresados.

### Requisitos

- `input()`
- `int()`
- variables
- `if / elif / else`
- `while` **o** `for`
- operadores aritméticos
- operadores relacionales
- `print()`

### Resolución
1er resolución:
```python
i = 1 #Contador
l = [] #Lista
p = [] #Positivos
n = [] #Negativos
c = [] #Ceros

while i <= 10:
    e = int(input('Ingresa un número entero: '))
    l.append(e) # Agrega un elemento al final de la lista.
    if e > 0:
        p.append(e)
    elif e == 0:
        c.append(e)
    else:
        n.append(e)
    i = i + 1

print('La cantidad de números positivos es', len(p), 'la cantidad de números negativos es', len(n), 'y la cantidad de números ceros es', len (c), '. El total es', sum(l)) # La función len() cuenta los elementos de un objeto.
```
2da resolución:
```python
i = 1 #Contador
s = 0 #Suma
p = 0 #Positivos
n = 0 #Negativos
c = 0 #Ceros

while i <= 10:
    e = int(input('Ingresa un número entero: '))
    s = s + e
    if e > 0:
        p = p + 1
    elif e == 0:
        c = c + 1
    else:
        n = n + 1
    i = i + 1

print('La cantidad de números positivos es', p, 'la cantidad de números negativos es', n, 'y la cantidad de números ceros es', c, '. El total es', s)
```
3er resolución:
```python
s = 0 #Suma
p = 0 #Positivos
n = 0 #Negativos
c = 0 #Ceros

#La función range() permite generar una secuencia de números 
for numero in range(10):
    e = int(input('Ingresa un número entero: '))
    s = s + e
    if e > 0:
        p = p + 1
    elif e == 0:
        c = c + 1
    else:
        n = n + 1

print('La cantidad de números positivos es', p, 'la cantidad de números negativos es', n, 'y la cantidad de números ceros es', c, '. El total es', s)
```