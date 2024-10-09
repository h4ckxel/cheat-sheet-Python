# 🐍 Cheat Sheet Python
Cheat Sheet en Python, diseñado para abarcar los conceptos básicos y algunos intermedios, incluyendo POO (Programación Orientada a Objetos). Este recurso ayudará a entender y practicar los elementos fundamentales del lenguaje.

---

### 1. **Conceptos Básicos**
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

#### Entrada y Salida de Datos
```python
nombre = input("¿Cómo te llamas? ")  # recibe entrada del usuario
print(f"Hola, {nombre}")             # salida con formato
```

### 2. **Operadores**
- **Aritméticos**: `+`, `-`, `*`, `/`, `//` (división entera), `%` (módulo), `**` (potencia)
- **Comparación**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Lógicos**: `and`, `or`, `not`
  
#### Ejemplo:
```python
a, b = 10, 20
print(a + b)          # suma
print(a == b)         # comparación
print(a > 5 and b < 30)  # operadores lógicos
```

### 3. **Estructuras de Control**
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

### 4. **Estructuras de Datos**
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

### 5. **Funciones**
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

### 6. **Manejo de Errores (Excepciones)**
```python
try:
    numero = int(input("Ingresa un número: "))
    print(f"El número es {numero}")
except ValueError:
    print("Eso no es un número válido")
```

### 7. **Módulos y Paquetes**
```python
import math
print(math.sqrt(16))  # raíz cuadrada
```
>[!NOTE]
En python para instalar el paquete es necesario hacerlo desde el kernel (***terminal***), por ejemplo para instalar "***math***". Se pone en la terminal ***`pip install math`***.
>

### 8. **Programación Orientada a Objetos (POO)**
#### Definición de Clases y Objetos
```python
class Persona:
    def __init__(self, nombre, edad):
        """constructor para inicializar atributos"""
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        """método para mostrar saludo"""
        print(f"Hola, soy {self.nombre} y tengo {self.edad} años")

# creación de objetos
persona1 = Persona("Acxel", 21)
persona1.saludar()
```

#### Herencia
```python
class Estudiante(Persona):
    def __init__(self, nombre, edad, carrera):
        """constructor para inicializar atributos heredados y nuevos"""
        super().__init__(nombre, edad)  # llamar al constructor de Persona
        self.carrera = carrera

    def mostrar_carrera(self):
        """método específico de estudiante"""
        print(f"Estudio {self.carrera}")

# creación de objeto Estudiante
estudiante1 = Estudiante("Acxel", 21, "Ingeniería en Software")
estudiante1.saludar()
estudiante1.mostrar_carrera()
```

### 9. **Lectura y Escritura de Archivos**
```python
# abrir un archivo en modo escritura
with open("archivo.txt", "w") as archivo:
    archivo.write("Esto es un archivo de prueba")

# abrir el archivo en modo lectura
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)
```

### 10. **Listas por Compresión**
```python
# crear una lista con los cuadrados de los números del 1 al 10
cuadrados = [x**2 for x in range(1, 11)]
print(cuadrados)
```

### 11. **Funciones Lambda y Map/Filter**
```python
# función lambda para calcular el cuadrado de un número
cuadrado = lambda x: x**2
print(cuadrado(5))

# usar map para aplicar una función a cada elemento de una lista
numeros = [1, 2, 3, 4, 5]
numeros_cuadrados = list(map(cuadrado, numeros))
print(numeros_cuadrados)

# usar filter para filtrar elementos de una lista
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)
```

### 12. **Uso de `__name__` y Scripts**
```python
# si este archivo se ejecuta como script, se ejecuta la siguiente función
def main():
    print("Este es un script en Python")

if __name__ == "__main__":
    main()
```

### 13. **Decoradores**
```python
def decorador(func):
    def nueva_funcion(*args, **kwargs):
        print("Ejecutando la función decorada...")
        resultado = func(*args, **kwargs)
        print("Función ejecutada.")
        return resultado
    return nueva_funcion

@decorador
def suma(a, b):
    return a + b

print(suma(5, 7))
```

---


<details>
<summary><b>Tips para Principiantes en Python</b></summary>

## 1. **Domina lo Básico Antes de Ir Más Allá**
- Antes de saltar a conceptos avanzados como POO o módulos complejos, asegúrate de entender bien las estructuras de control, tipos de datos y funciones.
- Trabaja en pequeños proyectos que utilicen conceptos básicos, como:
  - **Calculadoras simples**
  - **Juegos de adivinanza**
  - **Contadores de palabras**

## 2. **Practica Regularmente con Proyectos Pequeños**
- La programación es como aprender un nuevo idioma: solo mejoras si practicas.
- Empieza con pequeños proyectos como:
  - Calculadoras sencillas
  - Conversores de unidades (temperatura, longitud, etc.)
  - Creador de contraseñas aleatorias

## 3. **Lee y Escribe Código Regularmente**
- **Lee código de otros desarrolladores** para entender cómo estructuran sus programas y resuelven problemas.
- **Comenta tu propio código** para reforzar tu comprensión.
- **Explora repositorios en GitHub** y prueba contribuciones en proyectos pequeños.

## 4. **No Memorices, Entiende**
- Es mejor entender cómo funcionan los conceptos que tratar de memorizar código.
- Usa recursos como la [documentación oficial de Python](https://docs.python.org/3/) para despejar dudas.

## 5. **Utiliza el `print()` para Depuración**
- Al principio, usa `print()` para ver el valor de las variables en diferentes partes del código.
  
  ```python
  x = 10
  y = 5
  print(f"Valor de x: {x}, Valor de y: {y}")  # Muestra los valores actuales
  resultado = x + y
  print(f"Resultado: {resultado}")

### 6. **Trabaja con el Entorno Interactivo (REPL)**
- El entorno interactivo de Python (`python` o `ipython` en la terminal) es perfecto para probar rápidamente pequeñas porciones de código y entender su comportamiento.
- Puedes probar funciones, estructuras de control, listas y mucho más en tiempo real.
  
  ```python
  # Prueba rápidamente operaciones matemáticas y funciones simples
  >>> x = 10
  >>> y = 5
  >>> x + y
  15
  ```

### 7. **Aprende a Usar List Comprehensions**
- Las **List Comprehensions** son una manera eficiente y legible de manipular listas y colecciones.
  
  ```python
  # Crear una lista con los cuadrados de los primeros 10 números
  cuadrados = [x**2 for x in range(10)]
  print(cuadrados)  # salida: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
  ```

- Puedes agregar condiciones dentro de las comprehensions:

  ```python
  # Crear una lista solo con números pares del 0 al 9
  pares = [x for x in range(10) if x % 2 == 0]
  print(pares)  # salida: [0, 2, 4, 6, 8]
  ```

### 8. **Usa Nombres Descriptivos para Variables y Funciones**
- Elige nombres que indiquen claramente qué está almacenando la variable o qué hace la función.
  
  ❌ `a = 10`  
  ✔️ `total_ventas = 10`

- Esto mejora la legibilidad y el mantenimiento de tu código, especialmente cuando el proyecto crece.
  
  ```python
  # ejemplo con nombres descriptivos
  def calcular_area_triangulo(base, altura):
      return base * altura / 2
  ```

### 9. **Divide y Vencerás: Crea Funciones Pequeñas**
- No intentes hacer todo en una sola función larga. Divide el código en funciones pequeñas y específicas.
- Esto facilita la lectura, depuración y prueba del código.
  
  ```python
  def sumar(a, b):
      return a + b

  def restar(a, b):
      return a - b
  ```

- Utiliza nombres de funciones que indiquen claramente lo que hacen.

### 10. **Aprende a Usar el Depurador (`pdb`)**
- Python incluye un módulo llamado `pdb` que te permite pausar la ejecución y explorar el estado del programa.
- Útil para encontrar errores y entender el flujo de tu código.

  ```python
  import pdb
  pdb.set_trace()  # Pausa el programa aquí y permite inspeccionar variables
  ```

- Usa comandos como `n` (next), `c` (continue), `q` (quit) para moverte dentro del depurador.

### 11. **No Tengas Miedo de Consultar la Documentación**
- La [documentación oficial de Python](https://docs.python.org/3/) es tu mejor amigo.
- Puedes acceder a la documentación de cualquier módulo integrado con `help()`.

  ```python
  # muestra la documentación del método 'split' en cadenas
  help(str.split)
  ```

### 12. **Entiende los Errores y Excepciones**
- Aprende a leer los mensajes de error y qué significan.
- La mayoría de los errores comunes como `SyntaxError`, `NameError`, `IndexError` tienen un significado específico.
- Usa `try-except` para manejar errores y hacer tu código más robusto:

  ```python
  try:
      resultado = 10 / 0
  except ZeroDivisionError:
      print("No se puede dividir entre cero")
  ```

### 13. **Usa Formato de Cadenas (`f-strings`) para Facilitar la Legibilidad**
- En lugar de usar `format()` o concatenar con `+`, usa `f-strings` para insertar valores en cadenas:

  ```python
  nombre = "Juan"
  edad = 30
  print(f"Hola, {nombre}. Tienes {edad} años.")  # salida: Hola, Juan. Tienes 30 años.
  ```

### 14. **No Reinventes la Rueda: Conoce las Librerías Estándar**
- Python tiene muchas librerías incorporadas que pueden hacer muchas tareas por ti.
- Algunas útiles para principiantes:
  - `math` para operaciones matemáticas
  - `random` para generar números aleatorios
  - `datetime` para trabajar con fechas y horas

### 15. **Pide Ayuda y Únete a la Comunidad**
- No dudes en hacer preguntas en comunidades como [StackOverflow](https://stackoverflow.com/), foros de Python y grupos de chat.
- Programar es más fácil cuando compartes el conocimiento y resuelves problemas con otros.

</details>

*Este cheat sheet fue hecho por [h4ckxel](https://github.com/h4ckxel). ¡Buena suerte aprendiendo un nuevo lenguaje!*

---
















