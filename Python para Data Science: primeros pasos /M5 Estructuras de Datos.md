Apuntes Modulo 5 Estructuras de Datos en Python 🐍
--
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
# 📚 **Listas en Python**  

## 📌 **Cantidad de Elementos**  
Puedes utilizar la función `len()` para saber cuántos elementos hay en una lista.  
> **Recuerda**: Los índices comienzan desde `0`.  

#### 🛠️ *Ejemplo:*  
```python
libros = ["El principito", "1984", "Don Quijote"]
cantidad = len(libros)
cantidad  # Resultado: 3
```
## ✅ **Conclusión**  
- Usa `len()` para obtener la cantidad de elementos.
---

## ✂️ **Notación de Corte (Slice Notation)**  
Permite seleccionar porciones de una lista.  

- **Lista `[inicio:fin]`** → Extrae elementos entre el índice `inicio` y `fin - 1`.  
- **Lista `[inicio:]`** → Extrae elementos desde `inicio` hasta el final de la lista.  

#### 🛠️ *Ejemplo:*  
```python
libros = ["El principito", "1984", "Don Quijote", "Cien años de soledad", "Los miserables"]
seleccion = libros[0:2]  # Toma los elementos en las posiciones 0 y 1 (excluye el índice 2)
seleccion  # Resultado: ["El principito", "1984"]

desde_indice = libros[2:]  # Toma desde el índice 2 hasta el final
desde_indice  # Resultado: ["Don Quijote", "Cien años de soledad", "Los miserables"]
```
## ✅ **Conclusión**  
- Utiliza **slice notation** para seleccionar partes de una lista.  
---

## 🛠️ **Métodos de Lista**  
Las listas tienen métodos útiles para manipular sus elementos.  

### 🔹 **`append()` → Añadir un solo elemento al final**  
```python
libros = ["El principito", "1984"]
libros.append("Don Quijote")
libros  # Resultado: ["El principito", "1984", "Don Quijote"]
```

### 🔹 **`extend()` → Añadir múltiples elementos al final**  
```python
libros.extend(["Cien años de soledad", "Los miserables"])
libros  # Resultado: ["El principito", "1984", "Don Quijote", "Cien años de soledad", "Los miserables"]
```

### 🔹 **`remove()` → Eliminar un elemento específico**  
```python
libros.remove("1984")
libros  # Resultado: ["El principito", "Don Quijote", "Cien años de soledad", "Los miserables"]
```
## ✅ **Conclusión**    
- Modifica listas con `append()`, `extend()`, y `remove()`.  
---

## 👀 **Visualización de la Lista**  
Puedes imprimir la lista en cualquier momento para ver su contenido actual.  

#### 🛠️ *Ejemplo:*  
```python
print(libros)
```

📤 **Salida posible**:
```python
["El principito", "Don Quijote", "Cien años de soledad", "Los miserables"]
```
---
# 📚 **Manipulación de Listas en Python**

## 🔹 **`insert()` → Insertar un elemento en una posición específica**
- Permite **agregar** un elemento en una posición determinada dentro de la lista.
- **Sintaxis**: `lista.insert(indice, elemento)`

### 📖 *Ejemplo:* Insertar un libro en la posición 2
```python
libros = ["1984", "Cien años de soledad", "Los miserables"]
libros.insert(2, "Don Quijote")
libros  # Resultado: ["1984", "Cien años de soledad", "Don Quijote", "Los miserables"]
```
📌 *Nota:* `lista.insert(len(lista), elemento)` es equivalente a `append()`.

---

## 🔹 **`pop()` → Eliminar y devolver un elemento**
- **Elimina** el elemento en una posición específica y lo devuelve como resultado.
- **Sintaxis**: `lista.pop(indice)`

### 📖 *Ejemplo:* Eliminar el segundo libro de la lista
```python
libros = ["1984", "Cien años de soledad", "Los miserables"]
libro_eliminado = libros.pop(1)
libro_eliminado  # Resultado: "Cien años de soledad"
libros  # Resultado: ["1984", "Los miserables"]
```

---

## 🔹 **`index()` → Obtener el índice de un elemento**
- Devuelve el índice donde se encuentra **un elemento específico** dentro de la lista.
- **Sintaxis**: `lista.index(elemento)`

### 📖 *Ejemplo:* Encontrar la posición de "Los miserables"
```python
libros = ["1984", "Cien años de soledad", "Los miserables"]
posicion = libros.index("Los miserables")
posicion  # Resultado: 2
```

---

## 🔹 **`sort()` → Ordenar una lista**
- **Ordena** los elementos en **orden ascendente o descendente** (alfabético o numérico).
- **Sintaxis**: `lista.sort()`
- Para invertir el orden, usa `lista.sort(reverse=True)`

### 📖 *Ejemplo:* Ordenar una lista de libros
```python
libros = ["1984", "Cien años de soledad", "Los miserables", "Don Quijote"]
libros.sort()
libros  # Resultado: ["1984", "Cien años de soledad", "Don Quijote", "Los miserables"]
```

📌 *Orden descendente:*
```python
libros.sort(reverse=True)
libros  # Resultado: ["Los miserables", "Don Quijote", "Cien años de soledad", "1984"]
```

---

## ✅ **Resumen de Métodos**
| Método  | Función |
|---------|--------|
| `insert()` | Inserta un elemento en una posición específica |
| `pop()` | Elimina un elemento y lo devuelve |
| `index()` | Obtiene la posición de un elemento |
| `sort()` | Ordena la lista en orden ascendente o descendente |

---

# 📚 **Diccionarios en Python**  

## 📌 **¿Qué es un Diccionario?**  
- Son **colecciones de datos** que almacenan información en **pares clave-valor**.  
- La **clave** es un elemento único que identifica el valor en el diccionario.  
- Los **valores** pueden ser de cualquier tipo de dato.  
- No usan **índices numéricos**, sino claves únicas para acceder a los datos.  
- Son útiles para almacenar y acceder a datos de manera **organizada y rápida**.  

---

## 🏗 **Sintaxis y Ejemplo**  
Los diccionarios se crean usando **llaves `{}`** con la estructura `clave: valor`.  

```python
libro = {
    "titulo": "Cien años de soledad",
    "autor": "Gabriel García Márquez",
    "año": 1967,
    "genero": "Realismo mágico"
}
```

---

## 🔍 **Modificación**  
Para acceder o modificar valores en un diccionario:  

- **Acceder a un valor:**  
  ```python
  print(libro["titulo"])  # Salida: "Cien años de soledad"
  ```
- **Modificar un valor:**  
  ```python
  libro["genero"] = "Novela histórica"
  ```

---

## ➕ **Añadir Nuevos Elementos**  
Se pueden agregar nuevos pares clave-valor fácilmente:  

```python
libro["editorial"] = "Editorial Sudamericana"
```

---

## 📏 **Tamaño del Diccionario**  
Para conocer la cantidad de elementos en un diccionario:  

```python
len(libro)  # Devuelve el número de claves
```
---

