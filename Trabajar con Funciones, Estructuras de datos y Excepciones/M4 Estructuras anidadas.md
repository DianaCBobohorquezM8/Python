Apuntes ✨ Modulo 4 Estructuras Anidadas 🐍
---
# 🐍 List Comprehension y la función `zip()`

## ✅ ¿Qué es List Comprehension?

🔍 **List Comprehension** es una forma concisa y elegante de crear listas en Python. Permite aplicar operaciones y condicionales dentro de una única línea de código.

### 📌 Sintaxis básica:

```python
[expresión for elemento in iterable if condición]
```

### 🎯 Ejemplo:

```python
pares = [x for x in range(10) if x % 2 == 0]
print(pares)  # [0, 2, 4, 6, 8]
```

✅ Más legible
✅ Menos líneas de código
✅ Ideal para transformar o filtrar listas

---

## 🛠️ Funciones incorporadas útiles

### 🔄 `round()`

Redondea un número a un número específico de decimales.

```python
promedio = round(8.6666, 2)
print(promedio)  # 8.67
```

### 🔗 `zip()`

Combina varios iterables en **tuplas** elemento a elemento.

```python
nombres = ["Ana", "Luis", "María"]
edades = [23, 34, 28]
emparejados = list(zip(nombres, edades))
print(emparejados)  # [('Ana', 23), ('Luis', 34), ('María', 28)]
```

---

## 📊 Cálculo de Promedios con Listas Anidadas

Supongamos que cada sublista representa las calificaciones de un estudiante:

```python
calificaciones = [[9, 8, 7], [6, 5, 7], [10, 9, 10]]
promedios = [round(sum(est) / len(est), 2) for est in calificaciones]
print(promedios)  # [8.0, 6.0, 9.67]
```

---

## 🔍 Filtrado de Datos

Usa `List Comprehension` con condiciones para filtrar elementos.

### 🎯 Ejemplo: Estudiantes con promedio >= 8

```python
nombres = ["Ana", "Luis", "Carlos"]
promedios = [8.0, 6.0, 9.67]
aprobados = [(n, p) for n, p in zip(nombres, promedios) if p >= 8]
print(aprobados)  # [('Ana', 8.0), ('Carlos', 9.67)]
```

---

## 🧱 Estructuras de Datos en Python

### 📋 Listas

* Ordenadas
* **Mutables**
* Se pueden modificar después de su creación

```python
frutas = ["manzana", "pera"]
frutas.append("uva")
```

### 🔒 Tuplas

* Ordenadas
* **Inmutables**
* Útiles cuando los datos no deben cambiar

```python
usuario = ("Ana", 28, "Colombia")
```

---

## 🔠  Legibilidad del Código

👀 Un código legible:

* Usa nombres descriptivos
* Tiene estructura clara
* Usa comentarios cuando es necesario

```python
# Lista de estudiantes con nota mayor o igual a 8
aprobados = [(nombre, nota) for nombre, nota in zip(nombres, promedios) if nota >= 8]
```

📌 ¡La legibilidad es tan importante como la funcionalidad!

---

## 🔗 Profundizando en `zip()`

### 📌 Uso con un solo iterable:

```python
objeto_zip = zip([1, 2, 3])
print(list(objeto_zip))  # [(1,), (2,), (3,)]
```

⚠️ Cada elemento se agrupa como una tupla de un solo valor.

### 📌 Uso con múltiples iterables:

```python
id = [1, 2, 3, 4, 5]
region = ["Norte", "Oriente", "Sudeste", "Centro", "Sur"]

mapa = list(zip(id, region))
print(mapa)
# [(1, 'Norte'), (2, 'Oriente'), (3, 'Sudeste'), (4, 'Centro'), (5, 'Sur')]
```

---

## 🧮 ¿Qué pasa si los iterables tienen diferente longitud?

```python
codigos = ["1000", "1001", "1002", "1003", "1004", "1005"]
frutas = ["manzana", "uva", "banana", "naranja"]

mercancia = list(zip(codigos, frutas))
print(mercancia)
# [('1000', 'manzana'), ('1001', 'uva'), ('1002', 'banana'), ('1003', 'naranja')]
```

📌 La salida tiene la longitud del iterable más corto.

---

## 🔁 Desempaquetado Inverso con `*`

¿Tienes una lista de tuplas? Puedes **separarlas** fácilmente:

```python
tupla_iterable = [('J392', 'Juan'), ('M890', 'Maria'), ('J681', 'José')]
ids, nombres = zip(*tupla_iterable)

print(list(ids))     # ['J392', 'M890', 'J681']
print(list(nombres)) # ['Juan', 'Maria', 'José']
```
---

# 🐍 List Comprehension con `if` y `else`, Listas Anidadas y Aleatoriedad

📌 **List Comprehension** es una forma concisa y elegante de crear nuevas listas aplicando una operación o condición sobre los elementos de una lista existente o cualquier iterable.

### 🎯 Sintaxis básica:

```python
[expresión for elemento in iterable]
```

---

## ⚖️ Uso de `if` y `else` en List Comprehension

Puedes incluir condiciones con `if` y `else` directamente dentro de una List Comprehension para asignar valores de forma condicional.

### 📌 Sintaxis con condición ternaria:

```python
[expresión_true if condición else expresión_false for elemento in iterable]
```

### 🧪 Ejemplo:

```python
promedios = [6.5, 7.0, 8.3, 5.9]
situaciones = ["aprobado" if nota >= 7 else "reprobado" for nota in promedios]
print(situaciones)
# ['reprobado', 'aprobado', 'aprobado', 'reprobado']
```

---

## 🧱 Listas de Listas

Una **lista de listas** es una estructura que permite almacenar múltiples listas dentro de una lista principal. Es útil para representar **registros complejos**, como estudiantes con sus nombres, notas y estado.

### 📌 Ejemplo:

```python
nombres = ["Ana", "Luis", "Carlos"]
notas = [[8, 7, 9], [6, 5, 7], [9, 8, 9]]

registros = [[nombres[i], notas[i], round(sum(notas[i]) / len(notas[i]), 2)] for i in range(len(nombres))]
print(registros)
# [['Ana', [8, 7, 9], 8.0], ['Luis', [6, 5, 7], 6.0], ['Carlos', [9, 8, 9], 8.67]]
```

---

## 🧠 Agregando la situación (aprobado o reprobado)

Podemos extender la lista de listas para incluir la situación del estudiante según su promedio:

```python
registros = [
    [nombres[i], notas[i], promedio := round(sum(notas[i]) / len(notas[i]), 2), "aprobado" if promedio >= 7 else "reprobado"]
    for i in range(len(nombres))
]
```

### 🧾 Salida:

```python
[
    ['Ana', [8, 7, 9], 8.0, 'aprobado'],
    ['Luis', [6, 5, 7], 6.0, 'reprobado'],
    ['Carlos', [9, 8, 9], 8.67, 'aprobado']
]
```

---

## 🎲 Generación Aleatoria con `random`

Puedes generar códigos o valores aleatorios para simular datos usando el módulo `random`.

### 📌 Ejemplo: generar códigos aleatorios para estudiantes

```python
import random

nombres = ["Ana", "Luis", "Carlos"]
codigos = [f"ID{random.randint(100, 999)}" for _ in nombres]
print(codigos)
# ['ID742', 'ID683', 'ID915'] (puede variar cada vez que se ejecuta)
```
---
# 🐍 Python: Dict Comprehension 

## 🧠 ¿Qué es Dict Comprehension?

**Dict Comprehension** es una forma concisa y eficiente de crear diccionarios en Python, similar a la comprensión de listas pero utilizando llaves `{}` en lugar de corchetes `[]`.

🔹 Permite construir o modificar diccionarios aplicando operaciones a partir de **iterables** (como listas, tuplas o conjuntos).
🔹 También se pueden incluir **condicionales** para definir valores específicos bajo ciertas condiciones.

---

## 🧾 Sintaxis Básica

```python
{clave: valor for elemento in iterable}
```

🔁 También se pueden usar condicionales:

```python
{clave: valor for elemento in iterable if condición}
```

O incluir una condición ternaria:

```python
{clave: valor_si_true if condición else valor_si_false for elemento in iterable}
```

---

## 🛠️ Ejemplo Básico

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = {n: n**2 for n in numeros}
print(cuadrados)
# {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

---

## 🎓 Crear un Diccionario con Datos de Estudiantes

Supongamos que tenemos una lista de listas con los datos de varios estudiantes. Podemos convertir esa información en un diccionario organizado.

### 🧪 Datos:

```python
registros = [
    ['Ana', [8, 9, 7], 8.0, 'aprobado'],
    ['Luis', [5, 6, 7], 6.0, 'reprobado'],
    ['Carlos', [9, 9, 8], 8.67, 'aprobado']
]
```

### 🧰 Construcción del Diccionario:

```python
diccionario = {
    "estudiante": [r[0] for r in registros],
    "notas": [r[1] for r in registros],
    "promedio_final": [r[2] for r in registros],
    "situacion": [r[3] for r in registros]
}

print(diccionario)
```

### 📤 Salida:

```python
{
  'estudiante': ['Ana', 'Luis', 'Carlos'],
  'notas': [[8, 9, 7], [5, 6, 7], [9, 9, 8]],
  'promedio_final': [8.0, 6.0, 8.67],
  'situacion': ['aprobado', 'reprobado', 'aprobado']
}
```

---

## 🔁 Iteración para Crear Diccionarios

También puedes usar bucles `for` dentro de la comprensión de diccionarios para transformar datos, por ejemplo, para **filtrar aprobados**:

```python
aprobados = {r[0]: r[2] for r in registros if r[2] >= 7}
print(aprobados)
# {'Ana': 8.0, 'Carlos': 8.67}
```

---

