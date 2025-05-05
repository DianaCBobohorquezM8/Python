Apuntes Modulo 4 Estructuras de Repeticion en Python 🐍
---

## 🔁 Lazo `while` en Python

El bucle `while` es una **estructura de control** que permite ejecutar un bloque de código de forma repetida **mientras una condición sea verdadera**.

---

### 📌 **Definición**

El bucle `while` repite un bloque de instrucciones **tantas veces como sea necesario**, siempre que la condición especificada se mantenga como `True`.

---

### 🧱 **Sintaxis básica**

```python
while condición:
    # bloque de código a repetir
```

---

### 🔢 **Ejemplo: Contar del 1 al 10**

```python
contador = 1
while contador <= 10:
    print(contador)
    contador += 1  # Incremento elegante en Python
```

**Explicación:**

1. Se inicializa el contador en 1.  
2. La condición `contador <= 10` se evalúa en cada iteración.  
3. El número se imprime y se incrementa con `contador += 1`.

---
#### 🧪Ejemplo práctico:

Solicita dos notas y calcula el promedio para **2 estudiantes**, usando un bucle `while`.

```python
contador = 1

while contador <= 2:
    nota1 = float(input('Nota 1: '))
    nota2 = float(input('Nota 2: '))
    
    promedio = (nota1 + nota2) / 2
    print('Promedio:', promedio)
    
    contador += 1
```
#### ✅ ¿Qué hace este código?

- 🔁 Repite el proceso dos veces.
- 📥 Solicita dos notas por estudiante.
- 🧮 Calcula el promedio.
- 📤 Muestra el resultado.
- ➕ Aumenta el contador en cada vuelta del bucle.
---
## 🧾 Operadores de Asignación en Python

Los **operadores de asignación** permiten asignar un valor a una variable.

Por ejemplo:

```python
edad = 20
escolaridad = 'superior'
```

También existen **operadores compuestos** que modifican directamente el valor de una variable usando operaciones matemáticas:

---

## ➕ Operadores Compuestos de Asignación

| Operador | Descripción                                                                 | Ejemplo        |
|----------|-----------------------------------------------------------------------------|----------------|
| `+=`     | Suma un valor a la variable                                                 | `precio += 5`  |
| `-=`     | Resta un valor de la variable                                               | `precio -= 5`  |
| `*=`     | Multiplica la variable por un valor                                         | `precio *= 3`  |
| `/=`     | Divide la variable por un valor                                             | `precio /= 2`  |
| `//=`    | Realiza una **división entera** de la variable por un valor                | `precio //= 6` |
| `%=`     | Calcula el **residuo** de la división y lo asigna a la variable            | `precio %= 5`  |

---

### 🧪 Ejemplo práctico:

```python
precio = 100

precio += 10   # Ahora precio vale 110
precio -= 5    # Ahora precio vale 105
precio *= 2    # Ahora precio vale 210
precio /= 3    # Ahora precio vale 70.0
precio //= 4   # Ahora precio vale 17.0 (división entera)
precio %= 6    # Ahora precio vale 5.0 (residuo de 17 ÷ 6)

print(precio)  # Resultado final: 5.0
```
---
## 🔁 Lazo `for` en Python

El `for` es una estructura de **repetición** que permite **iterar** sobre un conjunto de elementos, como listas, cadenas o rangos numéricos. Se usa comúnmente cuando sabemos **cuántas veces** deseamos repetir una acción.

### 🧱 Estructura básica

```python
for elemento in conjunto:
    # bloque de código a ejecutar
```

El bloque se ejecuta **una vez por cada elemento** del conjunto. Cuando se han recorrido todos los elementos, el bucle se detiene automáticamente.

---

## 🔢 Función `range()`

La función `range()` genera una **secuencia de números enteros**. Puede recibir hasta tres argumentos:

- `inicio`: número donde comienza la secuencia (inclusive)
- `fin`: número donde termina la secuencia (exclusivo)
- `paso`: incremento entre valores (opcional, por defecto es 1)

```python
range(1, 6)  # Genera: 1, 2, 3, 4, 5
```

📌 El valor inicial es **inclusivo** y el final es **exclusivo**.

---

## ⚙️ Iteración automática

A diferencia del bucle `while`, en `for` no necesitas crear ni controlar un contador manualmente: Python se encarga de la iteración por ti.

---

## 🧪 Ejemplo básico

```python
for n in range(1, 11):
    print(n)
```

🔹 Este código imprime los números del **1 al 10**, uno por línea.

---

## 🏗️ Ejemplo aplicado: Propiedades construidas por año

El siguiente ejemplo usa un bucle `for` para calcular el total de propiedades construidas por una inmobiliaria entre 2017 y 2022:

```python
total_propiedades = 0

for año in range(2017, 2023):
    cantidad_propiedades = float(input(f'Digite la cantidad de propiedades en el año {año}: '))
    total_propiedades += cantidad_propiedades

print(f'Total de propiedades construidas: {total_propiedades} propiedades')
```

### 🧠 ¿Qué hace este código?

- Usa `range(2017, 2023)` para iterar desde 2017 hasta 2022.
- En cada vuelta del ciclo, solicita al usuario la cantidad de propiedades construidas ese año.
- Va **acumulando** las cantidades en la variable `total_propiedades`.
- Al finalizar, imprime el **total acumulado**.
---
¡Claro! Aquí tienes tu explicación mejorada y presentada en formato **Markdown**, con ejemplos claros y explicaciones breves para facilitar el aprendizaje:

---

## ⛓️ Comandos de Control en Bucles

Cuando usamos estructuras repetitivas como `for` o `while`, podemos controlar su flujo de ejecución utilizando los **comandos de control** `continue` y `break`. Estos comandos permiten **manipular el comportamiento del bucle** según ciertas condiciones.

---

### 🔁 `continue`

El comando `continue` **interrumpe solo la iteración actual** del bucle y **salta directamente a la siguiente**, omitiendo cualquier código restante en esa vuelta.

#### 📌 Ejemplo:
```python
for i in range(1, 6):
    if i == 4:
        continue
    print(i)
```

🔹 **Salida:**
```
1
2
3
5
```

➡️ Cuando `i` es igual a 4, la instrucción `continue` hace que **no se ejecute el `print(i)`** y pasa directamente a la siguiente vuelta.
### ✅ Conclusión
- Usa `continue` si quieres **saltar una vuelta específica** del bucle.
---

### 🛑 `break`

El comando `break` **detiene el bucle por completo**, incluso si no ha terminado de recorrer todos los elementos.

#### 📌 Ejemplo:
```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

🔹 **Salida:**
```
1
2
3
```

➡️ Cuando `i` es igual a 4, la instrucción `break` **rompe el bucle**, y ya no se ejecutan más iteraciones.

### ✅ Conclusión
- Usa `break` si quieres **detener el bucle completamente** bajo cierta condición.
---
# 📋 Listas en Python

## 📌 ¿Qué son las listas?

Las **listas** son estructuras de datos que permiten almacenar **colecciones ordenadas y mutables** de elementos.

---

## 🔧 Creación de listas

Se crean utilizando corchetes `[]`, separando los elementos con comas:

```python
frutas = ["manzana", "banana", "naranja"]
```

---

## 🧠 Tipos de datos

Las listas pueden contener cualquier tipo de dato:

```python
datos = [25, "Hola", 3.14, True, [1, 2, 3]]
```

---

## 🔢 Índices

* Los elementos se acceden por su posición (índice), que comienza en `0`.
* También puedes usar **índices negativos** para acceder desde el final.

```python
colores = ["rojo", "verde", "azul"]
print(colores[0])   # "rojo"
print(colores[-1])  # "azul"
```

---

## 🔄 Iteración sobre listas

Puedes recorrer los elementos de una lista usando un bucle `for`:

```python
for fruta in frutas:
    print(fruta)
```

---

## ✏️ Modificación de elementos

Puedes cambiar el valor de un elemento usando su índice:

```python
frutas[1] = "pera"
print(frutas)  # ["manzana", "pera", "naranja"]
```

---

## 📊 Cálculo de promedio

Si tienes una lista de números, puedes calcular el promedio:

```python
notas = [0, 4.0, 3.5, 5.0]  # índice 0 ignorado para facilitar ejemplo

promedio = (notas[1] + notas[2] + notas[3]) / 3
print(f"El promedio es: {promedio}"))
```
---
# 🧵 **Strings en Python** – Secuencia de Caracteres  

## 📌 **¿Qué es un String?**  
Un **string** es un tipo de dato que representa **texto**, compuesto por una **secuencia de caracteres** (letras, números, símbolos, etc.). Se puede definir utilizando comillas simples `'texto'` o dobles `"texto"`.

```python
lenguaje = 'Python'
```

---

## 🎯 **Acceso por Índice**  
Cada carácter dentro de un string tiene un **índice**, que comienza en `0` hasta `longitud - 1`. También es posible usar índices negativos para contar desde el final.

```python
print(lenguaje[0], lenguaje[1], lenguaje[2], lenguaje[-3], lenguaje[-2], lenguaje[-1])
```

📤 **Salida**:
```
P y t h o n
```

> ⚠️ **Los strings son inmutables**, lo que significa que no puedes modificar sus caracteres directamente.  
> Si intentas `lenguaje[0] = 'p'`, obtendrás un error.

---

## 🔁 **¿Los Strings Son Como Listas?**  
Pueden parecer similares porque se accede a sus caracteres mediante índices. Sin embargo:

- **Strings** → Son una secuencia de caracteres representados por **una sola variable**.
- **Listas** → Son estructuras que almacenan **varios elementos** (de distintos tipos) en **una sola variable**.

---

## 🧩 **Convertir un String en una Lista con `split()`**  
Podemos dividir un string en **una lista de subcadenas** utilizando un delimitador.

```python
pregunta = "¿Estoy aprendiendo? ¿Python? ¿O Mysql?"
lista_palabras = pregunta.split('?')
print(lista_palabras)
```

📤 **Salida**:
```python
['¿Estoy aprendiendo', ' ¿Python', ' ¿O Mysql', '']
```

🔹 **Dividir por espacios (sin especificar delimitador):**  
```python
lista_palabras = pregunta.split()
print(lista_palabras)
```

📤 **Salida**:
```python
['¿Estoy', 'aprendiendo?', '¿Python?', '¿O', 'Mysql?']
```

---

## 🔗 **Convertir una Lista en un String con `join()`**  
Podemos unir elementos de una lista en un solo string usando un **separador**.

```python
mezclas = [
    'Pinturas: rojo, azul y amarillo',
    'Verde: mezcla de azul y amarillo',
    'Naranja: mezcla de rojo y amarillo',
    'Morado: mezcla de rojo y azul'
]

unificador = '. '
cadena_mezclas = unificador.join(mezclas)
print(cadena_mezclas)
```

📤 **Salida**:
```
Pinturas: rojo, azul y amarillo. Verde: mezcla de azul y amarillo. Naranja: mezcla de rojo y amarillo. Morado: mezcla de rojo y azul.
```

---

## ✅ **Conclusión**  
- **Strings** son secuencias de caracteres **inmutables**.
- Podemos acceder a sus caracteres usando **índices**.
- Se pueden **convertir** en listas con `split()` y volver a strings con `join()`.

---
