
# Ejemplos de Uso de Funciones en Python

Este archivo contiene varios ejemplos sobre el uso de funciones en Python, utilizando la palabra clave `def`. Las funciones son bloques de código reutilizables que realizan tareas específicas. A continuación, se explican diferentes tipos de funciones con ejemplos prácticos.

## 1. Función con múltiples argumentos y `return`

Este ejemplo muestra cómo devolver múltiples valores desde una función:

```python
def operaciones_basicas(a, b):
    suma = a + b
    resta = a - b
    multiplicacion = a * b
    division = a / b if b != 0 else "Indefinida"  # Evita división por cero
    return suma, resta, multiplicacion, division

resultado = operaciones_basicas(10, 2)
print(f"Suma: {resultado[0]}, Resta: {resultado[1]}, Multiplicación: {resultado[2]}, División: {resultado[3]}")
```

## 2. Función con argumentos opcionales

Puedes establecer valores predeterminados para algunos argumentos, lo que los hace opcionales:

```python
def crear_saludo(nombre, saludo="Hola"):
    return f"{saludo}, {nombre}!"

print(crear_saludo("Carlos"))          # Usa el valor predeterminado de 'saludo'
print(crear_saludo("Ana", "Buenos días"))  # Usa un valor diferente para 'saludo'
```

## 3. Función que utiliza `*args` para múltiples argumentos

`*args` permite pasar un número variable de argumentos posicionales a la función:

```python
def sumar_todos(*numeros):
    return sum(numeros)

print(sumar_todos(1, 2, 3, 4, 5))  # Suma todos los números proporcionados
```

## 4. Función con `**kwargs` para argumentos con nombre

`**kwargs` permite pasar un número variable de argumentos con nombre a la función:

```python
def info_persona(**kwargs):
    for clave, valor en kwargs.items():
        print(f"{clave}: {valor}")

info_persona(nombre="Juan", edad=30, ciudad="Bogotá", profesion="Ingeniero")
```

## 5. Funciones como parámetros

En Python, las funciones pueden pasarse como parámetros a otras funciones:

```python
def aplicar_operacion(funcion, a, b):
    return funcion(a, b)

def multiplicar(x, y):
    return x * y

resultado = aplicar_operacion(multiplicar, 3, 4)
print(f"El resultado de la multiplicación es: {resultado}")
```

## 6. Funciones Lambda (Funciones anónimas)

Las funciones lambda son funciones pequeñas y anónimas que se pueden definir de forma compacta con `lambda`:

```python
# Función lambda para sumar dos números
suma_lambda = lambda a, b: a + b

# Función lambda como argumento
def aplicar_funcion(funcion, valor):
    return funcion(valor)

# Usando una función lambda
resultado = aplicar_funcion(lambda x: x ** 2, 5)
print(f"El cuadrado de 5 es: {resultado}")
```

## 7. Funciones recursivas

Una función puede llamarse a sí misma. Esto se llama **recursión**:

```python
def factorial(n):
    if n == 0 o n == 1:
        return 1
    else:
        return n * factorial(n - 1)

print(f"El factorial de 5 es: {factorial(5)}")
```

## 8. Funciones anidadas

Puedes definir una función dentro de otra función, y la función interna solo será accesible dentro de la función externa:

```python
def operacion_externa(x):
    def operacion_interna(y):
        return y ** 2
    return operacion_interna(x) + 1

print(operacion_externa(3))  # Llama a la función interna desde la externa
```

Este archivo incluye ejemplos comunes de uso de funciones en Python, con diferentes enfoques y aplicaciones. Las funciones permiten organizar y reutilizar código de forma eficiente.
