Apuntes ✨ Modulo 2 Funciones 🐍
---
# 📚 **Funciones en Python: Bloques de Código Reutilizables**

Las funciones son secuencias de instrucciones reutilizables que permiten organizar el código, hacerlo más legible y evitar la repetición.

### 📌 Funciones Incorporadas (Built-in Functions)

Python ofrece una serie de funciones que ya están integradas en el lenguaje y listas para ser usadas sin necesidad de importación. Esto proporciona una funcionalidad básica muy útil.

**Ventajas de las Funciones Incorporadas:**

* **🚀 Eficiencia:** Están optimizadas para un buen rendimiento.
* **💡 Facilidad de Uso:** No requieren implementación, se usan directamente.
* **✨ Abstracción:** Simplifican tareas complejas con interfaces sencillas.

### 📋 **Ejemplos de Funciones Incorporadas:**  
| Función | Descripción | Ejemplo |
|---------|------------|---------|
| `sum()` | Suma los valores en un iterable | `sum([1, 2, 3])` → `6` |
| `len()` | Devuelve la cantidad de elementos | `len([1, 2, 3])` → `3` |
| `round()` | Redondea un número | `round(8.165, 2)` → `8.17` |
| `abs()` | Devuelve el valor absoluto | `abs(-5)` → `5` |
| `bool()` | Convierte un valor a booleano | `bool(0)` → `False` |
| `dict()` | Crea un diccionario | `dict(nombre="Juan", edad=30)` |
| `pow()` | Calcula una potencia | `pow(2, 3)` → `8` |
| `input()` | Solicita entrada del usuario | `input("Nombre: ")` |
| `float()` | Convierte un valor a punto flotante | `float("3.14")` → `3.14` |

### 🏗 Tipos de Funciones en Python

🔹 Funciones sin Parámetros
Son aquellas que no reciben valores de entrada y se ejecutan directamente.
  ```python
def saludo():
    print("¡Hola, Python!")

saludo()  # Salida: ¡Hola, Python!
  ```
🔹 Funciones con Parámetros
Reciben uno o más valores (argumentos) que pueden utilizar dentro de su lógica.
  ```python
def promedio(nota1, nota2, nota3):
    return (nota1 + nota2 + nota3) / 3

print(promedio(8, 9, 7))  # Salida: 8.0
  ```
   ```python
    def saludar_a(nombre):
        print(f"¡Hola, {nombre}!")

    saludar_a("Dianadriel")
   ```

### 📋 Sintaxis para Definir Funciones

Se utiliza la palabra clave `def`, seguida del nombre de la función, paréntesis (que pueden contener parámetros) y dos puntos `:`. El bloque de código de la función va indentado debajo.

```python
def nombre_de_la_funcion(parametro1, parametro2, ...):
    # Instrucciones a ejecutar dentro de la función
    # ...
    return resultado  # Opcional: devuelve un valor
```

### Uso de Parámetros

* Se pueden definir múltiples parámetros separados por comas.
* Al llamar a la función, es importante proporcionar los argumentos en el orden correcto si no se utilizan nombres de parámetros (argumentos posicionales).

    ```python
    def sumar(a, b):
        resultado = a + b
        print(f"La suma de {a} y {b} es: {resultado}")

    sumar(5, 3)  # a toma el valor 5, b toma el valor 3
    ```

### 📌 Funciones con Listas

Las funciones pueden trabajar con listas para realizar operaciones sobre sus elementos.

```python
def calcular_promedio(notas):
    if not notas:
        return 0
    suma = sum(notas)
    promedio = suma / len(notas)
    return promedio

mis_notas = [85, 90, 78, 92]
promedio_final = calcular_promedio(mis_notas)
print(f"El promedio de las notas es: {promedio_final}")
```

### 🔄 Alcance de las Variables (Scope)

* Las variables definidas dentro de una función son **locales** y solo existen dentro de esa función. No se pueden acceder directamente desde fuera.
* Para que una función entregue un resultado al exterior, se utiliza la palabra clave `return`. Si no se usa `return`, la función implícitamente devuelve `None`.

    ```python
    def obtener_doble(numero):
        doble = numero * 2
        return doble

    resultado_doble = obtener_doble(7)
    print(f"El doble es: {resultado_doble}")
    # print(doble)  # Esto generaría un error porque 'doble' es local a la función
    ```

### Funciones en el Contexto de los Datos

Las funciones personalizadas son herramientas fundamentales en programación y ciencia de datos.

**Ventajas y Usos:**

* **♻️ Reutilización de Código:** Se pueden usar en diferentes partes del código, evitando repetición y mejorando la eficiencia y legibilidad.
* **🧹 Limpieza y 📊 Visualización de Datos:** Facilitan la automatización de tareas comunes como la limpieza de datos, la transformación y la creación de gráficos, permitiendo repetir estos procesos de manera rápida y eficiente.
* **🏗️ Organización y Mantenimiento:** Dividen el código en bloques lógicos más pequeños, lo que facilita la comprensión, el mantenimiento y la colaboración en proyectos grandes y complejos.
* **📤 Carga y Preprocesamiento de Datos:** Se utilizan frecuentemente para cargar datos de diversas fuentes (archivos, bases de datos, APIs) y realizar las etapas iniciales de preprocesamiento (filtrado, transformación, limpieza).
---
# 🧠 Uso de `return` y Tuplas en Funciones de Python

## 🔁 ¿Qué es `return` en Python?

La palabra clave `return` en Python se usa para **devolver valores desde una función** hacia el lugar donde se llamó. Es esencial cuando se desea **almacenar, reutilizar o procesar los resultados** de una función.

### 📌 Alcance de las Variables

* Las variables definidas dentro de una función tienen **alcance local**, es decir, solo existen durante la ejecución de esa función.
* Para **usar esos valores fuera de la función**, se debe utilizar `return`.

---

## 🧮 Ejemplo: Calcular el Promedio de Notas

```python
def calcular_promedio(notas):
    promedio = sum(notas) / len(notas)
    return promedio  # Retorna el valor calculado
```

```python
resultado = calcular_promedio([8, 7, 9])
print(f"El promedio es: {resultado}")
```

---

## 📊 Retornar Múltiples Valores con Tuplas

Las funciones también pueden devolver **más de un valor** al mismo tiempo utilizando **tuplas**.

### 🎓 Ejemplo: Promedio + Situación del Estudiante

```python
def boletin(notas):
    promedio = sum(notas) / len(notas)
    if promedio >= 7:
        situacion = "aprobado"
    else:
        situacion = "reprobado"
    return promedio, situacion  # Retorna una tupla
```

### 📥 Desempaquetado de la Tupla

```python
resultado, situacion = boletin([8, 7, 9])
print(f"Promedio: {resultado}, Situación: {situacion}")
```

| Elemento Retornado | Tipo    | Descripción                           |
| ------------------ | ------- | ------------------------------------- |
| `promedio`         | `float` | Resultado del promedio de las notas   |
| `situacion`        | `str`   | Texto que indica si fue aprobado o no |

---

## 📐 Ejemplo Práctico: Área y Perímetro de un Rectángulo

```python
def calcular_rectangulo(base, altura):
    area = base * altura
    perimetro = 2 * (base + altura)
    return area, perimetro  # Tupla con dos valores
```

```python
area, perimetro = calcular_rectangulo(5, 3)
print(f"Área: {area}, Perímetro: {perimetro}")
```

---

## 🧰 ¿Qué es una Tupla?

Una tupla es un tipo de estructura **inmutable** en Python que se define con paréntesis `()`.

### 🔎 Ejemplo de creación de tupla:

```python
mi_tupla = (1, 2, 3)
```

### 🎁 Ventajas de Usar Tuplas para Return

| Ventaja          | Descripción                                                             |
| ---------------- | ----------------------------------------------------------------------- |
| 🎯 Simplicidad   | Permiten devolver múltiples valores fácilmente.                         |
| 🔒 Inmutabilidad | Garantizan que los valores retornados no se modifiquen accidentalmente. |
| 💡 Legibilidad   | Hacen que el retorno de funciones sea más claro y organizado.           |

---

## 🔍 Dónde Ocurre la Tupla en el Código

```python
def boletin(notas):
    promedio = sum(notas) / len(notas)
    if promedio >= 7:
        situacion = "aprobado"
    else:
        situacion = "reprobado"
    
    return promedio, situacion  # Aquí se crea una tupla
```

```python
resultado, situacion = boletin([8, 7, 9])  # Aquí se desempaqueta la tupla
```

---

## 🖨️ Impresión de Resultados con `format` o f-strings

Puedes imprimir los resultados usando formatos:

```python
print("Promedio: {}, Situación: {}".format(resultado, situacion))
# o con f-string:
print(f"Promedio: {resultado}, Situación: {situacion}")
```
---



