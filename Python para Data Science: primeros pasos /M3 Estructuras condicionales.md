Apuntes Modulo 3 Estructuras condicionales en Python
---

## 🐍  **Estructuras Condicionales en Python** 🖥️ 
📖 Concepto
- Las estructuras condicionales permiten controlar el flujo de ejecución del código.
- Un bloque de código se ejecuta si se cumple una condición; en caso contrario, se ejecuta otro bloque.


📌 Palabras Clave
- if: Verifica si una condición es verdadera.
- else: Se utiliza junto con if para ejecutar un bloque si la condición es falsa.


🛠️ Sintaxis Básica
Solo if:
if condición:
    # código a ejecutar si la condición es verdadera


Con if y else:
if condición:
    # código si la condición es verdadera
else:
    # código si la condición es falsa

✨ Ejemplo
```python
if 2 < 7:
    print("La condición es verdadera")
else:
    print("La condición es falsa")
    
Salida: 'La condición es verdadera'
```

📝 Notas Importantes
- La indentación es crucial en Python: Usa 2 o 4 espacios de manera consistente para los bloques de código.
- El bloque else se ejecuta únicamente si la condición en el if es falsa.


🔄 Control de Flujo
- Facilita la toma de decisiones en el código.
- Permite ejecutar diferentes comandos según las condiciones definidas.

---
## ➕ 🧮 ➖ **Operadores Relacionales en Python**

### 📖 **Concepto**
- Los operadores relacionales comparan valores y determinan si una expresión es **verdadera** o **falsa**.
- Sirven para evaluar **condiciones** entre datos y devolver un resultado booleano.
  ⚖️
-  Los operadores relacionales son fundamentales para evaluar condiciones y tomar decisiones en programas 📚.
- Utilízalos para comparar cualquier tipo de datos, desde números y cadenas hasta información específica como libros.

---

## 🔹 **Operadores y Ejemplos**

### 1️⃣ **Mayor que (`>`)**
- **Descripción**: Devuelve `True` si el valor a la izquierda es **mayor** que el valor a la derecha; de lo contrario, devuelve `False`.
- **Ejemplo**: Comparar el número de páginas de dos libros.
  ```python
  paginas_libro1 = 350
  paginas_libro2 = 200
  paginas_libro1 > paginas_libro2  # Resultado: True
  ```

---

### 2️⃣ **Menor que (`<`)**
- **Descripción**: Devuelve `True` si el valor a la izquierda es **menor** que el valor a la derecha; de lo contrario, devuelve `False`.
- **Ejemplo**: Comparar años de publicación de dos libros.
  ```python
  año_libro1 = 1995
  año_libro2 = 2005
  año_libro1 < año_libro2  # Resultado: True
  ```

---

### 3️⃣ **Mayor o igual a (`>=`)**
- **Descripción**: Devuelve `True` si el valor a la izquierda es **mayor o igual** al valor a la derecha.
- **Ejemplo**: Comparar calificaciones de dos libros.
  ```python
  calificacion_libro1 = 4.8
  calificacion_libro2 = 4.8
  calificacion_libro1 >= calificacion_libro2  # Resultado: True
  ```

---

### 4️⃣ **Menor o igual a (`<=`)**
- **Descripción**: Devuelve `True` si el valor a la izquierda es **menor o igual** al valor a la derecha.
- **Ejemplo**: Verificar el número de capítulos de dos libros.
  ```python
  capitulos_libro1 = 12
  capitulos_libro2 = 15
  capitulos_libro1 <= capitulos_libro2  # Resultado: True
  ```

---

### 5️⃣ **Igual a (`==`)**
- **Descripción**: Devuelve `True` si los valores a ambos lados son **iguales**; de lo contrario, devuelve `False`.
- **Ejemplo**: Comparar títulos de dos libros.
  ```python
  titulo_libro1 = "El principito"
  titulo_libro2 = "El principito"
  titulo_libro1 == titulo_libro2  # Resultado: True
  ```

---

### 6️⃣ **Diferente de (`!=`)**
- **Descripción**: Devuelve `True` si los valores a ambos lados son **diferentes**; de lo contrario, devuelve `False`.
- **Ejemplo**: Comparar géneros de dos libros.
  ```python
  genero_libro1 = "Ficción"
  genero_libro2 = "No ficción"
  genero_libro1 != genero_libro2  # Resultado: True
  ```
---
## 🔀 Cláusula `elif` en Python

La cláusula `elif` se utiliza para **manejar múltiples condiciones** de forma más eficiente que usando solo `if` y `else`.

🧠 **Sintaxis básica**:
- Primero se evalúa una condición con `if`.
- Luego, se pueden usar uno o más `elif` para comprobar condiciones adicionales.
- Finalmente, se puede usar un `else` para manejar los casos que no cumplan ninguna de las condiciones anteriores.

📌 Esto permite que el programa **evalúe condiciones en cadena**, haciendo el código más limpio, legible y organizado.

💡 Puedes usar **varios `elif`** antes del `else`, lo que brinda **mayor flexibilidad** en la lógica del programa.

**Ejemplo**:  Clasificación de notas

```python
# Solicita la nota al usuario
nota = float(input('📥 Ingresa la nota del estudiante: '))

# Evalúa la nota usando if, elif y else
if nota >= 7:
    print('🏅 Aprobó')
elif 7 > nota >= 5:
    print('🛠️ Recuperación')
else:
    print('❌ No aprobó')
  ```

```python
# Supongamos que queremos clasificar una nota de un estudiante:
nota = 85

if nota >= 90:
    print("🏅 Excelente")
elif nota >= 80:
    print("👍 Muy bien")
elif nota >= 70:
    print("✅ Aprobado")
else:
    print("❌ Reprobado")
 ```
---
## 🔗 Operadores Lógicos y Cláusula `in` en Python

Los operadores lógicos `and`, `or` y `not` permiten **combinar múltiples condiciones** para controlar el flujo de un programa de forma más precisa.

---

### ⚙️ Operadores Lógicos

- **`and`** 🔐  
  La condición se cumple **solo si ambas expresiones son verdaderas**.  
  *Ejemplo:* `cond1 and cond2`

- **`or`** 🔓  
  La condición se cumple **si al menos una expresión es verdadera**.  
  *Ejemplo:* `cond1 or cond2`

- **`not`** 🔁  
  **Invierte** el valor lógico de una condición.  
  *Ejemplo:* `not cond`

---

### 📌 Cláusula `in`

La cláusula `in` se usa para **verificar si un elemento está presente** en una colección como una lista, tupla o cadena.

*Ejemplo:*  
```python
"Python" in ["Java", "Python", "C++"]  # Devuelve True

# Lista de estudiantes que aprobaron
aprobados = ["Ana", "Luis", "Carlos", "María"]

# Solicita el nombre del estudiante
nombre = input("📥 Ingresa el nombre del estudiante: ")

# Verifica si está en la lista de aprobados
if nombre in aprobados:
    print("🏅 ¡El estudiante aprobó!")
else:
    print("❌ El estudiante no está en la lista de aprobados.")
```
