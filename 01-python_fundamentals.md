---
title: Fundamentos de programación con Python
author: Cristobal Bergillos Navarro
date: 02-05-2024
---

# Presentacion

## ¿Quién soy yo?

- Ingeniero de Montes
- Técnico desarrollador de aplicaciones multiplataforma
- Experiencia con múltiples lenguajes de programación 

### RRSS

- *email*:   cristobalbergillostal@gmail.com
- *twitter*: @crisbernavarro

---

# Expectativas de esta ponencia

- Presentación ligera de cómo desarrollar con Python.
    - Aprender un lenguaje requiere mucho tiempo y trabajo.
    - No es realista pensar que después de esto vais a ser desarrolladores profesionales.
    - Demostrar que con poco tiempo y conocimientos se puede empezar.
    - La mayoría del contenido expuesto aquí podrá ser aplicado a otros lenguajes de programación.
- Captar vuestro interés para continuar por vuestra cuenta.
    - Gran cantidad de material gratuito en internet (videos, blogs, documentación... etc).
- Relajar el ritmo, prefiero dar poco contenido y que os quedéis con ganas de más a saturar vuestra atención. 
- Quemad el chat a preguntas, comentarios o lo que queráis. Voy a leerlo todo.

---

# ¿Por qué aprender a programar?

> Esto ya lo hace ChatGPT. Los programadores van a quedar obsoletos.

---

# ¿Por qué aprender a programar?

Estas son mis razones:

1. Es divertido. Consiste en resolver un puzzle.
2. Permite automatizar flujos de trabajo y eliminar ciertas tareas manuales.
3. Puedes crearte tus propias herramientas ajustadas a tus necesidades.

---

# ¿Cómo aprender a programar?

> Si no sé nada, ¿cómo empiezo?

1. Buscar un tutorial que contenga un proyecto.
2. Programar el proyecto del tutorial paso a paso.
3. Ampliar la funcionalidad del proyecto desarrollado en el tutorial (buscando más información en otras fuentes)
4. Repetir 1. -> 3. con varios proyectos
5. Desarrollar un proyecto personal desde cero o pequeñas herramientas que asistan a vuestro trabajo habitual

Esto puede llevar años, *disfrutad del proceso sin importar el tiempo dedicado.*

---

# ¿Por qué Python?

## Lenguaje multipropósito

Basicamente se puede programar de todo:

- Ciencia de datos y machine learning
- Deep learning
- Desarrollo de videojuegos
- Desarrollo web
- Aplicaciones de escritorio
- Scripting
- ... un largo etcétera

---

## ¿Por qué Python? > Facilidad de aprendizaje

Simplemente funciona. 

---

# ¿Por dónde empiezo a usar Python?

Python se puede usar directamente como calculadora.

Veamos un ejemplo.

---

# No tengo Python instalado... ¿Qué hago?

Existen intérpretes de python online, por lo que no es estrictamente necesario instalarlo localmente. 

Usaremos *Google Colab* para esta ponencia.

---

# Operaciones disponibles

- Operaciones con números enteros, decimales e incluso complejos
- Operadores:
    - Suma `+`
    - Resta `-`
    - Multiplicacion `*`
    - Potencia `**`
    - Divison `/`
    - Division entera `//`
    - Modulo `%` (resto de la division) 

---

# Variables

Los valores pueden ser almacenados en memoria como las calculadoras.

A ese espacio de memoria se le denomina *variable*. Consta de un nombre de la variable y su valor correspondiente.

Para mostrar el valor de las variables por consola, se puede usar la función `print()`

Por ejemplo:

```python
variable = 2
otra_variable = 2.3

resultado = variable + otra_variable
print(resultado)
```

---

# Tipos

El tipo de la variable indica qué clase de valor tiene asignado y que tipo de operaciones se pueden realizar sobre ella.

Acabamos de trabajar con dos tipos de datos distintos:
- `int()`
- `float()`

El tipo de una variable se puede consultar usando la función `type()`

Por ejemplo:

```python
variable = 2
print(type(variable))
```

---

# Tipos 

Python tiene muchos mas tipos de datos disponibles. Entre ellos:
- `str()`
- `list()`
- `dict()`

---

# Strings o cadenas

El tipo strings (`str()`) consiste en cadenas de texto. Una cadena de texto se define incluyendo texto entre `'...'` o `"..."`

Por ejemplo:

```python
cadena = "Hola que tal"
otra_forma = 'Hola que tal de nuevo'

print(cadena)
print(otra_forma)
```

---

# ¿Recordáis los tipos?

¿Qué pasa si utilizamos `+` con strings?

```python
print("Hola" + "Mundo") 
```

---

# ¿Recordáis los tipos?

Queda demostrado que *diferentes tipos* contienen *diferentes operaciones*.

---

# Otras características de las strings

Acceso a carácteres por posición utilizando `[]` 

```python
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
   0   1   2   3   4   5   
  -6  -5  -4  -3  -2  -1
```

Por ejemplo:

```python
palabra = "Python"
print(palabra[0])
print(palabra[3])
print(palabra[-1])
print(palabra[-5])
```

---

# Slices de una string

Además de acceder a un único carácter, se puede acceder a un rango de carácteres utilizando `[:]`.

Por ejemplo, para la cadena "Python", los límites del slice son los siguientes:

*Ojo que son diferentes a las posiciones anteriores*

```python
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1
```

Por tanto, se puede acceder a diferentes rangos de esta forma:

```python
palabra = "Python"

print(palabra[0:2])
print(palabra[3:-1])
```

---

# Obtener longitud de una string

Se puede consultar la longitud de una cadena usando la función `len()`

Por ejemplo:

```python
palabra = "Python"
print(len(palabra))
```

---

# Listas 

Son un nuevo tipo de datos llamado *tipos compuestos*:
- Tipo que agrupa diferentes valores.
- Valores separados por `,` dentro de `[]`.
- Puede contener valores de *diferentes tipos*.

Un ejemplo de lista sería:

```python
lista = [1, 3, 5, 6]
print(type(lista))
print(lista)
```

---

## Acceso a valores de una lista

A los valores de una lista se accede igual que a los carácteres dentro de un string

Por ejemplo:

```python
lista = [1, 2, 3, 4]
print(lista[0])
print(lista[-1])
print(lista[1:3])
```

---

## Cambio de valores en una lista

Se pueden cambiar los valores dentro de una lista accediendo al valor por su posición y cambiando su valor. 

Por ejemplo:

```python
lista = [1, 2, 3, 4]
print(lista)
lista[0] = 2
print(lista)
```

---

## Agregar valores a una lista

Se pueden agregar nuevos valores a una lista utilizando el método `list.append()`

Por ejemplo:

```python
lista = [1, 2, 3, 4]
print(lista)
lista.append(2)
print(lista)
```

---

## Eliminar valores de una lista

Para eliminar un valor de una lista se puede usar `del`

Por ejemplo:

```python
lista = [1, 2, 3, 4]
print(lista)
del lista[2]
print(lista)
```

---

## Número de elementos de una lista

De la misma forma que con los strings, se usa la función `len()` para ver el número de elementos que contiene.

Por ejemplo:

```python
lista = [1, 2, 3, 4]
print(len(lista))
```

---

# Diccionarios

Los diccionarios (`dict()`) son un tipo de datos compuesto que almacena los valores en un par *clave: valor*. 

Los diccionarios se definen entre `{}` a diferencia de las listas que se definen entre `[]`. 

La clave y los valores pueden ser de cualquier tipo, incluso dentro del mismo diccionario (aunque normalmente se use el mismo tipo para ambos)

Por ejemplo:

```python
diccionario = {"Cristobal": 3, "Nestor": 4}
print(diccionario)
```

Las claves en el diccionario `diccionario` son del tipo `str` mientras que los valores son del tipo `int`.

---

## Acceso a los valores de un diccionario

A los elementos de los diccionarios *se accede por la clave* y no por la posición.

Por ejemplo:

```python
diccionario = {"Cristobal": 3, "Nestor": 4}

# acceder al valor de Cristobal 
print(diccionario["Cristobal"])
```

---

## Otra propiedades de los diccionarios

El diccionario tiene propiedades similares a las listas:
- Se puede consultar los elementos que contiene con la función `len()`
- Se puede modificar el valor de una clave de la misma forma que una lista
- También se pueden eliminar los valores utilizando `del`

---

# ¿Dudas?

Ahora toca subir de nivel.

---

# Control de flujo

Todo lo visto anteriormente hace que Python funcione como una "calculadora" haciendo operaciones de forma lineal. 

El control de flujo permite que un programa:
- Tome decisiones sobre qué código ejecutar en función a unas *condiciones*.
- Ejecute código repetidamente con *bucles*.
- Saltar de una parte del código a otra y reutilizar código gracias a las *funciones*.

Esto supondrá un gran porcentaje de todo lo que se requiere para crear un programa funcional.

---

## Condicionales

Permiten ejecutar una parte de código u otra en base a una condición establecida.

Para ello se usarán las palabras reservadas `if`, `elif` y `else` (aunque estas dos últimas son opcionales)

---

### El tipo bool

El tipo de dato `bool()` puede tomar los valores `True` o `False` (atención a las mayúsculas en Python). 

Este valor puede ser almacenado en una variable o no, bastaría en algunos casos con declarar el valor

Por ejemplo:

```python
es_cierto = True
print(es_cierto)
es_falso = False
print(es_falso)
```

---

### Operadores lógicos

Ciertos operadores devuelven un valor bool al ser utilizados. Estos valores son:
- `>`, `<`, `>=` y `<=`
- `==` y `!=`

Se utilizan de esta forma:

```python
print(3 == 4)
print(3 > 4)
print(5 >= 4)
print(5 != 4)
```

---

## Condicionales

Los condicionales junto con los operadores lógicos permiten ejecutar una parte de código u otra. 

Por ejemplo: 

```python
nombre = "Nestor"
if nombre == "Cristobal":
    print("Soy yo")
else:
    print("Es Nestor")
```

---

## Condicionales

Se pueden hacer condicionales que contengan más opciones gracias a `elif`. 

Por ejemplo: 

```python
# Conversor a números romanos del 1 al 5
numero = 3

if numero == 1:
    print("I")
elif numero == 2:
    print("II")
elif numero == 3:
    print("III")
elif numero == 4:
    print("IV")
elif numero == 5:
    print("V")
else:
    print("El número es menor que 0 o mayor que 5")
```

---

## Bucles

Los bucles permiten ejecutar una parte de código repetidamente. 

Las dos formas más comunes para ejecutar un bucle son:
1. El bucle `for`
2. El bucle `while`

---

### Bucle for

El bucle `for` en Python es un poco especial. Es algo diferente a otros lenguajes por defecto. 

Permite iterar sobre elementos de una lista. 

Por ejemplo:

```python
lista = [1, 2, 3, 4]
for numero in lista:
    print("El numero es ", numero)
```

---

### Bucle for

Un ejemplo práctico del buble `for` sería para filtrar valores dentro de un diccionario.

El método `dict.items()` permite extraer los pares clave valor de un diccionario para ser iterados por el bucle `for`

Por ejemplo:

```python
# coleccion de usuarios
usuarios = {"Cristobal": "activo", "Nestor": "inactivo", "Carmen": "activo"}
print(usuarios)

# coleccion vacia
usuarios_activos = {}

# iterar las claves y valores de la coleccion usuarios
for usuario, status in usuarios.items():
    # si el status del usuario es "activo"
    if status == "activo":
        # almacena el usuario con su status en la nueva coleccion
        usuarios_activos[usuario] = status

print(usuarios_activos)
```

---

#### Función range

La función `range()` crea una lista de números. Se puede utilizar de 3 formas:
1. `range(int)`               -> Crea una lista desde el 0 hasta el número `int` de uno en uno
2. `range(start, stop)`       -> Crea una lista desde el número `start` hasta el `stop` (sin incluirlo) de uno en uno
3. `range(start, stop, step)` -> Crea una lista desde el número `start` hasta el `stop` (sin incluirlo) incrementando por `step`

Ejemplos:

```python
# 1. range(int)
for i in range(10):
    print(i, end=",")

print("")

# 2. range(start, stop)
for i in range(2, 10):
    print(i, end=",")

print("")

# 3. range(start, stop, step)
for i in range(5, 50, 5):
    print(i, end=",")
```

---

### Bucle while

El bucle `while` permite ejecutar repetidamente una parte de código *mientras se cumple una condición*. 

Por ejemplo:

```python
contador = 0

while contador < 10:
    print(contador)
    contador = contador + 1
```

---

### Cuándo usar un bucle for o while

Ambos bucles pueden ser usados para repetir partes de código de la misma forma. Sin embargo, es conveniente usar uno u otro para distintos casos:
- `for`   -> para iterar sobre colecciones o para repetir la instrucción un número finito de veces
- `while` -> para repetir la instrucción indefinidamente hasta que se cumpla la condición. 

---

# ¿Dudas?

Un respiro, por favor...

... No ha quedado más remedio que dejar para el final algo bastante complejo...

... Por suerte va a ser lo último.

---

## Funciones

Hemos usado diferentes funciones a lo largo de la ponencia como `len()`, `type()` o `range()`

Pero, ¿qué es una función?

---

## Funciones

Una función es un bloque de código que puede ser reutilizado en distintas partes del código.

Pensad en las funciones en matemáticas: *f(x) = ax + b*

---

## Funciones

Una función consta de las siguientes partes:
- Nombre               -> Deben tener un nombre para ser invocadas posteriormente
- Parámetros           -> Un parámetro es un valor que se le pasa a la función antes de ser invocada. Son opcionales. 
- Documentación        -> Descripción de lo que hace la función
- Cuerpo de la función -> Contiene la lógica de la función 
- Return               -> Valor que devuelve la función al terminar. Es opcional.

---

## Funciones

Una función se declara así:

```python
# el nombre de la funcion es sumar y tiene dos parametros: a y b
def sumar(a, b):
    """Función que suma los parámetro a y b"""
    # logica de la funcion
    resultado = a + b

    # valor que devuelve la funcion
    return resultado

# la funcion se invoca asi
suma = sumar(3, 2)
print(suma)
```

---

## Funciones

¿Para qué sirve esto?

Declarar funciones tiene grandes beneficios:

- Puedes reutilizar las funciones tantas veces como quieras dentro del código.
- Las funciones reducen la complejidad del código ocultando su lógica.
- Puedes empaquetar las funciones y compartirlas para que otros puedan usarlas. 

---

## Funciones

Vamos a crear funciones que calculen:

1. El radio y perimetro de una circunferencia.
2. Las horas, minutos y segundos a partir de los segundos especificados como parametro.
3. La media de los valores de una lista de número enteros.
