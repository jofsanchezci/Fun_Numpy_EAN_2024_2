
# Guía de Uso Básico de NumPy

Este archivo proporciona una descripción básica de cómo usar la biblioteca NumPy para cálculos numéricos en Python. NumPy es una de las bibliotecas más utilizadas en ciencia de datos y cálculo numérico.

## Instalación

Para instalar NumPy, utiliza el siguiente comando:

```bash
pip install numpy
```

## Importar NumPy

Normalmente, NumPy se importa con el alias `np`:

```python
import numpy as np
```

## Creación de Arrays

### Array Unidimensional:

```python
import numpy as np

# Crear un array unidimensional
a = np.array([1, 2, 3, 4, 5])
print(a)
```

### Array Bidimensional:

```python
# Crear un array bidimensional
b = np.array([[1, 2, 3], [4, 5, 6]])
print(b)
```

### Arrays con valores iniciales:

```python
# Crear un array de ceros
zeros = np.zeros((3, 3))
print(zeros)

# Crear un array de unos
ones = np.ones((2, 4))
print(ones)

# Crear un array con valores aleatorios
random_array = np.random.random((3, 3))
print(random_array)
```

## Operaciones con Arrays

### Operaciones aritméticas básicas:

```python
a = np.array([1, 2, 3, 4, 5])
b = np.array([10, 20, 30, 40, 50])

# Sumar dos arrays
suma = a + b
print(suma)

# Multiplicar dos arrays
multiplicacion = a * b
print(multiplicacion)

# Elevar cada elemento al cuadrado
cuadrado = a ** 2
print(cuadrado)
```

### Funciones estadísticas:

```python
a = np.array([1, 2, 3, 4, 5])

print("Media:", np.mean(a))
print("Desviación estándar:", np.std(a))
print("Suma de todos los elementos:", np.sum(a))
```

### Multiplicación de matrices:

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

# Producto punto
producto = np.dot(A, B)
print(producto)
```

## Indexación y Rebanado

### Indexación simple:

```python
a = np.array([1, 2, 3, 4, 5])

# Acceder a un elemento
print(a[0])  # Primer elemento

# Acceder a un rango de elementos
print(a[1:4])  # Elementos desde la posición 1 a la 3
```

### Indexación en arrays multidimensionales:

```python
b = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Acceder a un elemento en una matriz
print(b[0, 2])  # Elemento en la primera fila, tercera columna

# Rebanar una submatriz
print(b[0:2, 1:3])  # Submatriz con las dos primeras filas y columnas 1 a 2
```

## Cambio de forma (Reshape)

```python
a = np.array([[1, 2, 3], [4, 5, 6]])

# Cambiar la forma a un array de 3x2
reshaped = a.reshape(3, 2)
print(reshaped)
```

## Comparaciones y Operaciones Lógicas

```python
a = np.array([1, 2, 3, 4, 5])

# Comparar cada elemento con 3
print(a > 3)  # [False False False  True  True]

# Filtrar elementos mayores a 3
print(a[a > 3])  # [4 5]
```

## Álgebra Lineal

```python
from numpy.linalg import inv, det

A = np.array([[1, 2], [3, 4]])

# Inversa de una matriz
inversa = inv(A)
print(inversa)

# Determinante de una matriz
determinante = det(A)
print(determinante)
```

---

Esta guía cubre los conceptos básicos del uso de NumPy. Es una biblioteca fundamental para cualquier proyecto que implique cálculos numéricos en Python. Puedes explorar más características avanzadas en la [documentación oficial de NumPy](https://numpy.org/doc/).
