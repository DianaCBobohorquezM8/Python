Apuntes Modulo 2 Manipulando datos en Python
---
## 📝 **Comentarios en Python**

### ✏️ *¿Qué son los comentarios?*
- Los comentarios son anotaciones dentro del código que **no se ejecutan ni interpretan**.
- **Propósito**: Explican el funcionamiento del código, ayudan a otras personas (o a ti misma) a entender mejor su lógica, y son esenciales para documentar funciones, estructuras o métodos.
- **Ventaja**: Hacen que el código sea más legible y fácil de mantener.

---

## 🖥️ **Tipos de comentarios**

### 🔹 *Comentarios de una línea*
- Comienzan con el símbolo `#`.
 **Ejemplo**:
  ```python
  # Este es un comentario de una línea
  nombre = "Jesús"  # Este comentario explica la asignación de la variable
  ```

### 🔹 *Comentarios de varias líneas*
- Se pueden escribir utilizando triple comillas (`'''` o `"""`).
 **Ejemplo**:
  ```python
  '''
  Este es un comentario de varias líneas.
  Se utiliza para explicar etapas completas del código o agregar documentación.
  '''
  ```

---


## 🐍 **Definición de Variables en Python**

### ✏️ *¿Qué son las variables?*
- Las variables se definen asignando un **nombre**, seguido del signo igual (**=**) y el **valor** que almacenarán.
- **Ejemplo**:  
  ```python
  nombre = "Jesús"
  edad = 33
  ```
---
## ⚙️ **Reglas para Nombrar Variables**
1. **No comenzar con números**:  
   - Ejemplo incorrecto: `10_notas`
2. **No usar espacios en los nombres**:  
   - Ejemplo incorrecto: `nombre escuela`
3. **Evitar palabras reservadas de Python**, como:
   - `False`, `None`, `True`, `and`, `as`, `assert`, `break`, `class`, `continue`, `def`, `del`, `elif`, `else`, `except`, `finally`, `for`, `from`, `global`, `if`, `import`, `in`, `is`, `lambda`, `nonlocal`, `not`, `or`, `pass`, `raise`, `return`, `try`, `while`, `with`, `yield`.
4. Las **mayúsculas y minúsculas** se consideran variables distintas.
   - Ejemplo: `Edad` y `edad` son diferentes.

---

## 🛠️ **Ejemplo adicional para observar reutilización de memoria**
### Variables con el mismo valor:
```python
nombre1 = "Jesús"
nombre2 = "Jesús"
print(id(nombre1))  # Dirección de memoria de nombre1
print(id(nombre2))  # Dirección de memoria de nombre2 (será igual a nombre1 porque tienen el mismo valor)
```
---
## 🖥️ **Función `id`**
- Permite conocer la dirección de memoria de un objeto.
- **Nota**: Las variables pueden apuntar al mismo espacio de memoria si almacenan el mismo valor.

### 🛠️ *Ejemplo para observar el espacio en memoria*
```python
nombre = "Jesús"
edad = 33
ciudad = "Nazaret"

print(id(nombre))  # Dirección de memoria de la variable nombre
print(id(edad))    # Dirección de memoria de la variable edad
print(id(ciudad))  # Dirección de memoria de la variable ciudad
```
---
## 📌 **Tipos Principales de Variables en Python**

### 1️⃣ **Enteros (`int`)**
- **Descripción**: Representan números enteros (sin decimales).
- **Ejemplo**:  
  ```python
  edad = 5
  print(type(edad))  # Verifica que la variable es de tipo 'int'
  ```

### 2️⃣ **Flotantes (`float`)**
- **Descripción**: Representan números con decimales.
- **Ejemplo**:  
  ```python
  promedio = 9.5
  print(type(promedio))  # Verifica que la variable es de tipo 'float'
  ```

### 3️⃣ **Cadenas de caracteres (`string`)**
- **Descripción**: Representan texto. Se pueden definir usando comillas simples (`'`) o dobles (`"`).
- **Ejemplo**:  
  ```python
  nombre_estudiante = "Jesús"
  print(type(nombre_estudiante))  # Verifica que la variable es de tipo 'str'
  ```

### 4️⃣ **Booleanos (`bool`)**
- **Descripción**: Representan valores de verdadero (**True**) o falso (**False**).
- **Ejemplo**:  
  ```python
  situacion_academica = True
  print(type(situacion_academica))  # Verifica que la variable es de tipo 'bool'
  ```

---

### 🛠️ *Uso de la función `type()` para verificar tipos*
La función `type()` se utiliza para comprobar el tipo de datos de una variable en Python. Aquí tienes un ejemplo práctico para verificar múltiples variables:

```python
# Declaración de variables
nombre = "Jesús"
edad = 33
promedio = 10
es_estudiante = True

# Verificación del tipo de cada variable
print(type(nombre))         # Resultado: <class 'str'>
print(type(edad))           # Resultado: <class 'int'>
print(type(promedio))       # Resultado: <class 'float'>
print(type(es_estudiante))  # Resultado: <class 'bool'>
```
---


