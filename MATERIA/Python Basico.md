- Es un lenguaje de programación fácil de leer que permite asignación de variables, operaciones matemáticas.
![[Pasted image 20230727111921.png]]
***
==FUNCIONES Y AYUDA== 
Incluye la ayuda integrada, los argumentos por defecto, las funciones que no devuelven valores y las funciones de orden superior.
***
==Listas==
Son secuencias ordenadas de valores que pueden ser **modificadas** e **indexadas**, también ofrecen funciones útiles para manipularlas. 
***
==Bucles y compresión de listas==
los bucles en Python (for, while) repiten código determinado. las comprensiones de listas permiten condensar bucles y condicionales en una sola linea.
***
==Strings y Diccionarios==
Las cadenas son flexibles e inmutables, soportando múltiples métodos de manipulación. las listas y diccionarios también son útiles para organizar datos.
***
==Trabajando con librerias externas==
Python permite la importación de librerías, ya sea **estándar** o **personalizadas**, a través de importaciones. las librerías contienen módulos que son colecciones de funciones y valores.
***
tres opciones si se gana o no cualquier cantidad 
posibilidad de cambio de boleto cuando no gane el anterior 
cuando no gane nada 
4 numeros el boleto y un animal a traves del mismo animal tener otro boleto gratis 
***
==EJEMPLOS==
***
Ejemplo 1: Suma de dos números ingresados por el usuario

```python
def suma_numeros():
    try:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
        resultado = num1 + num2
        print("La suma es:", resultado)
    except ValueError:
        print("Error: Ingresa números válidos.")

suma_numeros()
```
***
Ejemplo 2: Cálculo del factorial de un número

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

numero = int(input("Ingresa un número para calcular su factorial: "))
if numero < 0:
    print("Error: Ingresa un número positivo o cero.")
else:
    print("El factorial de", numero, "es:", factorial(numero))
```
***
Ejemplo 3: Clase para representar un círculo y calcular su área y circunferencia

```python
import math

class Circulo:
    def __init__(self, radio):
        self.radio = radio

    def area(self):
        return math.pi * self.radio ** 2

    def circunferencia(self):
        return 2 * math.pi * self.radio

radio_circulo = float(input("Ingresa el radio del círculo: "))
mi_circulo = Circulo(radio_circulo)
print("Área del círculo:", mi_circulo.area())
print("Circunferencia del círculo:", mi_circulo.circunferencia())
```
