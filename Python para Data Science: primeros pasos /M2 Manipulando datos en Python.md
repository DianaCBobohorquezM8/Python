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
## 📌 **Tipos Principales de Variables en Python**  🐍

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
## 💾 Almacenamiento y 🧠 Gestión de Memoria en Transformaciones de Cadenas (Python) 🐍

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
## ➕ **Operadores Aritméticos Adicionales en Python** 🐍

### 🔹 **Exponenciación (`**`)**
- **Descripción**: Eleva un número a una potencia.
- Ejemplo con variables:
  ```python
  base = 2
  exponente = 3
  resultado_expo = base ** exponente
  resultado_expo  # Resultado: 8
  ```
- Ejemplo Sin variables:
  ```python
  2 ** 3  # Resultado: 8
  ```

### 🔹 **Módulo (`%`)**
- **Descripción**: Devuelve el residuo de una división entera.
- Ejemplo con variables:
  ```python
  dividendo = 7
  divisor = 3
  residuo = dividendo % divisor
  residuo  # Resultado: 1
  ```
Ejemplo Sin variables:
  ```python
  7 % 3  # Resultado: 1
  ```

### 🔹 **División Entera (`//`)**
- **Descripción**: Devuelve solo la parte entera de una división.
  (el residuo de una división es decir el número que queda cuando la división no es exacta)
- Ejemplo con variables:
  ```python
  dividendo = 7
  divisor = 3
  cociente_entero = dividendo // divisor
  cociente_entero  # Resultado: 2
  ```
Ejemplo Sin variables:
  ```python
  7 // 3  # Resultado: 2
  ```
---
## 🖥️ **Capturando Datos en Python**

### 1️⃣ **Función `input`**
- Permite recolectar datos del usuario.
- **Nota**: El valor ingresado siempre será de tipo `string`, incluso si parece un número.

#### 🛠️ *Ejemplo relacionado:*
```python
nombre = input("¿Cuál es tu nombre?")
```
El valor almacenado en la variable será el texto `"Jesús"`.

---

### 2️⃣ **Almacenamiento en Variables**
- Es importante guardar los datos recolectados en **variables** para utilizarlos posteriormente en el programa.

#### 🛠️ *Ejemplo relacionado:*
```python
edad = input("¿Qué edad tienes?")
```
*Imaginemos que se ingresa*: `"33"`.

---

### 3️⃣ **Conversión de Tipos**
- Si necesitas realizar operaciones matemáticas, convierte el valor recolectado de `string` a otro tipo:
  - **Enteros**: `int(dato)`
  - **Flotantes**: `float(dato)`
  - **Cadenas de texto**: `str(dato)`
  - **Booleanos**: `bool(dato)`

#### 🛠️ *Ejemplo relacionado:*
```python
edad = int(input("¿Qué edad tienes?"))
```
Si Jesús responde `"33"`, el valor en la variable `edad` será el número entero `33`.

---

### 4️⃣ **Presentación de Resultados**
- Usa la función `format` para insertar variables en cadenas de texto y mejorar la presentación.
- También permite agregar formatos como:
  - **Nueva línea**: `\n`
  - **Tabulación**: `\t`

#### 🛠️ *Ejemplo relacionado:*
```python
nombre = input("¿Cuál es tu nombre?")
edad = int(input("¿Qué edad tienes?"))
ciudad = input("¿De dónde eres?")

mensaje = "Hola, {}.\nTienes {} años.\nVives en:\t{}.".format(nombre, edad, ciudad)
mensaje
```
*Si Jesús de Nazaret responde:*
- Nombre: `"Jesús"`
- Edad: `"33"`
- Ciudad: `"Nazaret"`

El resultado será:
```
Hola, Jesús.
Tienes 33 años.
Vives en:    Nazaret.
```
### ✅ **Notas Importantes**
1. Captura los datos con `input()` y guárdalos en variables.
2. Usa las funciones de conversión si necesitas trabajar con datos no textuales.
3. Mejora la presentación de los resultados con `format` y formatos especiales.
---
## 📝 **Tabla Unicode**

### 🌍 **¿Qué es Unicode?**
- Es una **tabla de codificación de caracteres** que asocia códigos numéricos con caracteres específicos.
- Su objetivo es incluir caracteres de **todos los idiomas y sistemas de escritura** existentes en el mundo.
- En la versión **15.0**, Unicode ya agrupa más de **140,000 caracteres**, incluyendo letras, números, símbolos y emojis.

### 🔁 **¿Por qué es importante?**
- Unicode nació como una alternativa a tablas más limitadas, como **ASCII**, que solo admitía caracteres del alfabeto inglés y algunos símbolos.
- Es fundamental para la **globalización**, ya que permite representar caracteres de diferentes idiomas de manera:
  - **Consistente:** Sin importar el dispositivo o la plataforma.
  - **Precisa:** Incluyendo caracteres como "ç" (portugués), "ñ" (español) o "П" (ruso).
- La tabla **se actualiza constantemente** para garantizar la inclusión de más idiomas y sistemas de escritura.

### 🌐 **¿Dónde consultar las actualizaciones?**
- Puedes acceder al estándar Unicode y sus codificaciones en:
  - **[unicode.org](https://unicode.org)**
---

## 🖥️ **Usando Unicode en Python**

### 🔹 **Función `chr`**
- Devuelve el carácter que corresponde a un **código Unicode** específico.
- **Sintaxis**: `chr(número_del_carácter)`

#### 🛠️ *Ejemplo 1: Imprimir un carácter*
```python
# Obtener el carácter "@", cuyo código Unicode es 64
chr(64)
# Salida: '@'
```

#### 🛠️ *Ejemplo 2: Construir palabras*
Podemos usar `chr` junto con el operador `+` para concatenar caracteres y formar palabras:
```python
# Construir la palabra "Hola"
chr(72) + chr(111) + chr(108) + chr(97)
# Salida: 'Hola'
```
### 🧪 **Experimentando y probando combinaciones**

# Ejemplo 1: Caracteres especiales
```python
caracter1 = chr(36)   # Código 36 es '$'
caracter2 = chr(169)  # Código 169 es '©'
caracter3 = chr(174)  # Código 174 es '®'
`
# Resultado
caracter1, caracter2, caracter3
# Salida: '$', '©', '®'
```
# Ejemplo 2: Letras y símbolos
```python
letra = chr(65)       # Código 65 es 'A'
simbolo = chr(9733)   # Código 9733 es '★'

# Resultado
letra, simbolo
# Salida: 'A', '★'
```
# Ejemplo 3: Emojis con Unicode
```python
carita_feliz = chr(128522)  # Código 128522 es '🙂'
carita_triste = chr(128542) # Código 128542 es '😢'
corazon = chr(10084)        # Código 10084 es '❤'

# Resultado
carita_feliz + " " + carita_triste + " " + corazon
# Salida: '🙂 😢 ❤'
```
---

