Apuntes Modulo 2 Manipulando datos en Python
---
## 🐍  **Cómo usar la documentación en python.org** 📚

### ✏️ *¿Por qué debería usarla?*
- Para comprender mejor la **sintaxis y estructuras** al trabajar en mis proyectos de programación.
- Como referencia sobre **bibliotecas y herramientas**, ya que me interesa optimizar mis proyectos relacionados con Data Science y Automatización.
- Para aprender más sobre **funciones y métodos** que me ayuden a implementar soluciones eficientes.
- Para estudiar **ejemplos de código** que complementen mi aprendizaje práctico.

### 🎯 *¿Cómo puede ayudarme?*
- **Como principiante**: Para dominar los fundamentos del lenguaje y reforzar lo aprendido en mis ejercicios y proyectos personales.
- **Como referencia avanzada**: Cuando necesito explorar temas más específicos mientras desarrollo mis proyectos de programación.

### 📂 *Organización para mi estudio*
1. **Temas clave**: Investigar temas relacionados con mis intereses, como:
   - Manipulación de datos.
   - Creación de scripts automáticos.
   - Visualización de datos.
2. **Bibliotecas útiles**: Familiarizarme con aquellas que necesito, como NumPy, Pandas, y Matplotlib.
3. **Documentar mi progreso**: Tomar notas importantes para consolidar mi aprendizaje y resolver dudas más rápido.

### 🔗 *Acceso*
Puedo consultarla directamente en [python.org](https://www.python.org/doc/) para avanzar en mis objetivos de aprendizaje y mejorar mis proyectos.

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
## 📝 **Ejercicio: Análisis de Salarios y Empleados**

### 📊 **Tabla de información**

| Cargo         | Cantidad | Salario |
|---------------|----------|---------|
| Vigilante     | 5        | 300     |
| Docente       | 16       | 500     |
| Coordinador   | 2        | 600     |

---

### 🎯 **Objetivos**
1. Calcular la **cantidad total de empleados**.
2. Determinar la **diferencia entre el salario más bajo y más alto**.
3. Calcular el **promedio ponderado de los salarios**.

---
### 🔢 **Cálculos y Código**

#### 1️⃣ *Cantidad total de empleados*
Suma de todos los empleados:

```python
c_vigilante = 5
c_docente = 16
c_coordinador = 2

# Cálculo total de empleados
total_empleados = c_vigilante + c_docente + c_coordinador
total_empleados
```

#### 2️⃣ *Diferencia entre el salario más bajo y más alto*
Resta entre el salario más alto (coordinador) y el más bajo (vigilante):

```python
s_vigilante = 300
s_docente = 500
s_coordinador = 600

# Cálculo de la diferencia
diferencia_salario = s_coordinador - s_vigilante
diferencia_salario
```

#### 3️⃣ *Promedio ponderado de los salarios*
Para calcularlo:
- Multiplicamos la cantidad de empleados por sus respectivos salarios.
- Sumamos los resultados y dividimos por la cantidad total de empleados.

```python
# Cálculo del promedio ponderado de los salarios
promedio_salarios = (c_vigilante * s_vigilante + c_docente * s_docente + c_coordinador * s_coordinador) / total_empleados
promedio_salarios
```

---
### ✅ **Resultados esperados**
Después de ejecutar el código:
1. **Cantidad total de empleados**: 23.
2. **Diferencia entre salario más bajo y más alto**: 300.
3. **Promedio ponderado de los salarios**: 465.22 (aproximadamente).
---
## 📝 **Variables de texto en Python**

### ✏️ *¿Qué es  `String`?*
- Un **string** es una colección de caracteres alfanuméricos que se define colocando el contenido entre comillas simples (`'`) o dobles (`"`).  
- **Ejemplo**:  
  ```python
  t = 'Diana Bohorquez'
  type(t)  # Verifica que la variable es de tipo 'str'
  ```

### 🖥️ *Las variables textuales son objetos*
- Como objetos, las variables de tipo `string` tienen **métodos** que permiten manipular o editar el texto contenido en ellas.

---

## 🛠️ **Métodos de los `String`**

### ✨ *¿Cómo funcionan los métodos?*
- Los métodos son funciones asociadas a los objetos que permiten realizar operaciones en ellos.  
- La sintaxis es: `objeto.metodo()`.  
- **Nota**: Algunos métodos no requieren el uso de paréntesis `()`.

---

### 🔹 **Métodos útiles para strings**

#### 1️⃣ `str.upper()`
- **Función**: Convierte una string a **mayúsculas**.
- **Ejemplo**:  *.upper()*
  ```python
  texto = "hola mundo"
  texto_mayusculas = texto.upper()
  print(texto_mayusculas)  # Resultado: 'HOLA MUNDO'
  ```

#### 2️⃣ `str.lower()`
- **Función**: Convierte una string a **minúsculas**.
- **Ejemplo**: *.lower()*
  ```python
  texto = "HOLA MUNDO"
  texto_minusculas = texto.lower()
  print(texto_minusculas)  # Resultado: 'hola mundo'
  ```

#### 3️⃣ `str.strip()`
- **Función**: Elimina los **espacios en blanco** al inicio y al final de una string.
- **Ejemplo**:  *.strip()*
  ```python
  texto = "  hola mundo  "
  texto_limpio = texto.strip()
  print(texto_limpio)  # Resultado: 'hola mundo'
  ```

#### 4️⃣ `str.replace(antiguo, nuevo)`
- **Función**: Sustituye todas las ocurrencias del texto `"antiguo"` en la string por el texto `"nuevo"`.
- **Ejemplo**:  *.replace('antiguo', 'nuevo')*
  ```python
  texto = "Python es divertido"
  texto_nuevo = texto.replace("divertido", "fantástico")
  print(texto_nuevo)  # Resultado: 'Python es fantástico'
  ```
---
## 💾 Almacenamiento y 🧠 Gestión de Memoria en Transformaciones de Cadenas (Python)

**🔑 Punto Clave:** Para que las modificaciones realizadas a una cadena de texto en Python se guarden de forma permanente, es crucial **asignar el resultado de la transformación a una nueva variable**.

**Explicación:**

* **🧱 Inmutabilidad de las Cadenas:** En Python, las cadenas son inmutables. Esto significa que las operaciones de transformación (como `strip()`, `replace()`, `upper()`, etc.) no modifican la cadena original. En cambio, **✨ crean una nueva cadena** con los cambios aplicados.

* **➡️ Almacenamiento de Cambios:** Si no se asigna el resultado de estas operaciones a una nueva variable, la cadena original permanecerá sin cambios 🚫 y la nueva cadena generada se perderá 💨.

* **⚙️ Gestión de Memoria:**
    * Las variables en Python actúan como **🏷️ referencias a ubicaciones específicas en la memoria** donde se almacenan los datos (en este caso, las cadenas de texto).
    * Cuando se asigna una transformación a una nueva variable, esta variable apunta a una **📍 nueva ubicación de memoria** que contiene la cadena modificada.
    * El **🗑️ recolector de basura (garbage collector)** de Python se encarga de liberar la memoria que ya no está siendo utilizada por ninguna variable. Cuando una variable deja de ser necesaria (por ejemplo, si se redefine sin guardar la referencia anterior), la memoria a la que apuntaba eventualmente se libera.

### 🔢 **Ejemplo práctico con resultados**

#### Caso 1️⃣: Almacenar cambios en una nueva variable

```python
texto = "  Python es divertido y útil  "
**nuevo_texto** = texto.strip().replace('y', 'ó').upper()

# Resultados esperados
**nuevo_texto**
# Resultado: 'PYTHON ES DIVERTIDO Ó ÚTIL'

id(texto), id(nuevo_texto)
# Resultado: Dos identificadores diferentes porque 'texto' y 'nuevo_texto' ocupan espacios distintos en la memoria.
```
##### ✅ **Resumen de comportamiento esperado**
- **Caso 1**: Se conserva el valor original en `texto` y se asigna el texto modificado a una nueva variable `nuevo_texto`.

#### Caso 2️⃣: Actualizar directamente la misma variable

```python
**texto** = texto.strip().replace('y', 'ó').upper()

# Resultados esperados
**texto**
# Resultado: 'PYTHON ES DIVERTIDO Ó ÚTIL'

id(texto), id(nuevo_texto)
# Resultado: Diferentes identificadores; 'texto' apuntará a un nuevo espacio en memoria con el resultado de la transformación, mientras que 'nuevo_texto' conservará su memoria original.
```
##### ✅ **Resumen de comportamiento esperado**
- **Caso 2**: La variable `texto` se modifica directamente y apunta a un nuevo espacio de memoria con los cambios realizados.
---


