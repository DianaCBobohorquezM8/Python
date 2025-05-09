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
