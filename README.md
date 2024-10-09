# 🐍 Cheat Sheet Python
Cheat Sheet en Python, diseñado para abarcar los conceptos básicos y algunos intermedios, incluyendo POO (Programación Orientada a Objetos). Este recurso ayudará a entender y practicar los elementos fundamentales del lenguaje.

### 1. Conceptos Básicos

#### Comentarios
```python
# Comentario de una sola línea
"""
Comentario de
varias líneas
"""
```
#### Variables
```python
nombre = "Acxel"        # cadena de texto (string)
edad = 20               # entero (int)
altura = 1.75           # número con decimales (float)
es_programador = True   # booleano (True/False)
```
#### Entrada y Salida de datos
```python
nombre = input("¿Cómo te llamas? ")  # recibe entrada del usuario
print(f"Hola, {nombre}")             # salida con formato
```
### 2. Operadores
- Aritméticos: `+, -, *, /, // (división entera), % (módulo), ** (potencia)`
- Comparación: `==, !=, <, >, <=, >=`
- Lógicos: `and, or, not`
##### Ejemplo:
```python
a, b = 10, 20
print(a + b)          # suma
print(a == b)         # comparación
print(a > 5 and b < 30)  # operadores lógicos
```
### 3. Estructuras de control
#### Condicionales
```python
edad = 18
if edad >= 18:
    print("Eres mayor de edad")
elif 13 <= edad < 18:
    print("Eres adolescente")
else:
    print("Eres niño")
```
#### Bucles
```python
# bucle while
contador = 0
while contador < 5:
    print(contador)
    contador += 1

# bucle for con rango
for i in range(5):
    print(i)

# bucle for con listas
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    print(fruta)
```
### 4. Estructuras de datos
#### Listas
```python
numeros = [1, 2, 3, 4, 5]  # lista de enteros
print(numeros[0])          # acceso a elementos (primer elemento)

# métodos comunes
numeros.append(6)          # agrega un elemento
numeros.remove(3)          # elimina el valor 3
print(len(numeros))        # longitud de la lista
```
#### Tuplas
```python
coordenadas = (10, 20)  # tupla inmutable
print(coordenadas[0])   # acceso a elementos
```
#### Diccionarios
```python
estudiante = {
    "nombre": "Acxel",
    "edad": 21,
    "carrera": "Ingeniería en Software"
}
print(estudiante["nombre"])  # acceso a elementos

# agregar y modificar valores
estudiante["edad"] = 22
estudiante["promedio"] = 9.5
```
#### Conjuntos
```python
# conjuntos no permiten elementos duplicados
numeros_unicos = {1, 2, 3, 4, 5}
numeros_unicos.add(6)
numeros_unicos.remove(4)
```
### 5. Funciones
```python
def saludar(nombre):
    """función que recibe un nombre y saluda"""
    print(f"Hola, {nombre}")

def sumar(a, b):
    """función que retorna la suma de dos números"""
    return a + b

saludar("Acxel")          # llamada a la función
print(sumar(10, 5))       # resultado de la suma
```
### 6. Manejo de errores (Excepciones)
```python
try:
    numero = int(input("Ingresa un número: "))
    print(f"El número es {numero}")
except ValueError:
    print("Eso no es un número válido")
```
### Módulos y paquetes
```python
import math
print(math.sqrt(16))  # raíz cuadrada
```
>[!NOTE] Nota
En python para instalar el paquete es necesario hacerlo desde el kernel (***terminal***), por ejemplo para instalar "***math***". Se pone en la terminal ***`pip install math`***.
>
```python```
```python```
```python```
```python```
```python```















