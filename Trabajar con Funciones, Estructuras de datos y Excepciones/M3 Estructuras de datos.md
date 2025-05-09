Apuntes ✨ Modulo 3 Estructuras de Datos 🐍
---

# 📚 Listas de Listas en Python

Las **listas de listas** son estructuras de datos anidadas que permiten almacenar y manipular conjuntos de datos más complejos, como tablas, matrices o agrupaciones jerárquicas.

---

## 🧱 ¿Qué son?

Las **listas de listas** son estructuras donde cada elemento puede ser otra lista. Se usan para representar datos organizados en múltiples dimensiones (como filas y columnas).

```python
# Ejemplo simple
matriz = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

---

## 🛠️ Separando Nombres y Calificaciones

Supongamos que tienes una lista que contiene **nombres de estudiantes y sus calificaciones**, como esta:

```python
datos = ['Ana', 8, 9, 7, 'Luis', 6, 5, 8, 'María', 9, 10, 8]
```

### 🎯 Objetivo:

Separar esta lista en dos nuevas listas:

* `nombres`: contiene solo los nombres.
* `notas`: contiene solo las calificaciones.

---

## 🔢 Uso de Índices e Iteración

Se puede usar el operador **módulo (%)** para identificar los nombres (en posiciones múltiplos de 4) y las notas (los demás índices).

```python
nombres = []
notas = []

for i in range(len(datos)):
    if i % 4 == 0:
        nombres.append(datos[i])
    else:
        notas.append(datos[i])
```

---

## 🧮 Agrupación en Listas de Listas

Agrupamos las calificaciones en sublistas de tres elementos (una por estudiante):

```python
notas_separadas = []

for i in range(0, len(notas), 3):
    grupo = notas[i:i+3]
    notas_separadas.append(grupo)
```

### 📋 Resultado:

```python
print(nombres)         # ['Ana', 'Luis', 'María']
print(notas_separadas) # [[8, 9, 7], [6, 5, 8], [9, 10, 8]]
```

---

## ✅ Ventajas de las Listas de Listas

| 🧠 Característica        | ✅ Beneficio                                                    |
| ------------------------ | -------------------------------------------------------------- |
| 📦 Estructura jerárquica | Permite organizar datos complejos (como filas y columnas)      |
| 📊 Formato tipo tabla    | Facilita análisis como el cálculo de promedios o comparaciones |
| 🔄 Iteración organizada  | Permite recorrer y procesar datos en grupos                    |
| 🔍 Lectura clara         | Aumenta la legibilidad del código en análisis de datos         |

---

## 🧪 Ejemplo completo

```python
datos = ['Ana', 8, 9, 7, 'Luis', 6, 5, 8, 'María', 9, 10, 8]

# Listas vacías
nombres = []
notas = []

# Separar nombres y notas
for i in range(len(datos)):
    if i % 4 == 0:
        nombres.append(datos[i])
    else:
        notas.append(datos[i])

# Agrupar notas en listas de tres
notas_separadas = []
for i in range(0, len(notas), 3):
    grupo = notas[i:i+3]
    notas_separadas.append(grupo)

# Mostrar resultados
print("Nombres:", nombres)
print("Notas por estudiante:", notas_separadas)
```

---

## 🧠 Conclusión

Las **listas de listas** permiten:

* ✅ Almacenar datos de múltiples dimensiones
* ✅ Organizar estructuras similares a tablas o matrices
* ✅ Facilitar el análisis de datos en ciencia de datos, educación, etc.

Son fundamentales cuando se necesita **agrupar o estructurar datos jerárquicamente** para mejorar la lógica del programa y su eficiencia.

---

# 📘 Listas de Tuplas en Python

Las **tuplas** son estructuras de datos **inmutables**, ideales para agrupar información que **no debe cambiarse** una vez definida.

---

## 🧱 ¿Qué es una tupla?

Una tupla se define con **paréntesis `()`** y puede contener múltiples elementos separados por comas.

```python
registro = ("Julia", 23, "CDMX", "EM", "Python para DS 1")
```

---

## 🔍 Acceso a elementos

Se accede por **índices**, como en las listas:

```python
print(registro[0])   # Julia
print(registro[-1])  # Python para DS 1
```

---

## 📦 Desempaquetado

Las tuplas pueden desempaquetarse para asignar sus valores a variables:

```python
nombre, edad, ciudad, estado, curso = registro
print(f"La estudiante {nombre} tiene {edad} años y vive en {ciudad}-{estado}. Ella está matriculada en el curso de {curso}.")
```

### ✅ Salida:

```
La estudiante Julia tiene 23 años y vive en CDMX-EM. Ella está matriculada en el curso de Python para DS 1.
```

---

## 🆚 Listas vs Tuplas

| Característica | Listas 🔁 (listas) | Tuplas 🔒 (tuplas) |
| -------------- | ------------------ | ------------------ |
| Mutabilidad    | ✅ Mutables         | ❌ Inmutables       |
| Uso            | Datos cambiantes   | Datos fijos        |
| Símbolo        | `[]`               | `()`               |

---

## 🎯 Objetivo: Lista de tuplas con códigos únicos

Queremos crear una **lista de tuplas** donde cada tupla contenga:

1. Nombre del estudiante
2. Un código único generado con:

   * La primera letra del nombre
   * Un número aleatorio entre 0 y 999

---

## 🧮 Paso a paso

### 1️⃣ Lista de nombres

```python
nombres = ["Ana", "Luis", "María", "Carlos"]
```

---

### 2️⃣ Importamos `randint` y definimos función

```python
from random import randint

def genera_numero():
    return randint(0, 999)
```

---

### 3️⃣ Creamos lista vacía para almacenar las tuplas

```python
codigo_estudiantes = []
```

---

### 4️⃣ Generamos las tuplas

```python
for i in range(len(nombres)):
    codigo = nombres[i][0] + str(genera_numero())
    codigo_estudiantes.append((nombres[i], codigo))
```

---

### ✅ Resultado:

```python
print(codigo_estudiantes)
```

#### 💡 Salida ejemplo:

```python
[('Ana', 'A723'), ('Luis', 'L085'), ('María', 'M210'), ('Carlos', 'C993')]
```

---

## 🧠 ¿Por qué usar tuplas aquí?

✅ Son **más ligeras** y rápidas que las listas
✅ Protegen los datos de modificaciones accidentales
✅ Funcionan bien como **pares clave-valor** agrupados

---

## 🎓 Conclusión

Las **listas de tuplas** permiten:

* Agrupar datos relacionados
* Mantener su inmutabilidad (importante para integridad de datos)
* Ser utilizadas como registros simples (tipo fila en una base de datos)

---

