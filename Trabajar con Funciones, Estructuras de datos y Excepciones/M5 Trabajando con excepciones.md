Apuntes ✨ Modulo 5 Excepciones 🐍
---
# ⚠️ Manejo de Excepciones en Python

El manejo de **excepciones** en Python es fundamental para crear programas robustos, prevenir errores inesperados y mejorar la experiencia del usuario.

---

## 🧨 ¿Qué son las excepciones?

En Python, existen dos tipos de errores:

1. **Errores de sintaxis**:

   * Son detectados al momento de interpretar el código.
   * Impiden que el programa se ejecute.

2. **Excepciones**:

   * Son errores que ocurren **durante la ejecución** del programa.
   * Si no son manejadas, **interrumpen el flujo** y pueden cerrar el programa.

> 📚 Consulta la [jerarquía oficial de excepciones de Python](https://docs.python.org/es/3/library/exceptions.html#exception-hierarchy)

---

## 🔧 ¿Por qué tratar las excepciones?

✅ Permite mantener el programa funcionando
✅ Proporciona mensajes más comprensibles al usuario
✅ Evita comportamientos inesperados en el análisis de datos o interacción con el sistema

---

## 🧱 Estructura básica: `try` y `except`

```python
try:
    # Código que puede generar una excepción
except NombreDeLaExcepcion as e:
    # Código que se ejecuta si ocurre esa excepción
```

### 🧪 Ejemplo básico

```python
try:
    numero = int(input("Ingresa un número: "))
    print("El doble es:", numero * 2)
except ValueError as e:
    print("❌ Error: Debes ingresar un número válido.")
```

---

## 🧩 Clausulas adicionales: `else` y `finally`

| Cláusula  | ¿Cuándo se ejecuta?                                                                 |
| --------- | ----------------------------------------------------------------------------------- |
| `else`    | Solo si **no ocurre ninguna excepción**                                             |
| `finally` | Siempre se ejecuta, ocurra o no una excepción (ideal para cerrar archivos, limpiar) |

### 💡 Ejemplo completo:

```python
try:
    estudiantes = {"Ana": 9.0, "Luis": 7.5}
    nota = estudiantes["Carlos"]
except KeyError:
    print("⚠️ Estudiante no encontrado.")
else:
    print("✅ Nota del estudiante:", nota)
finally:
    print("🎓 Fin del proceso.")
```

---

## 🛑 Captura genérica de excepciones

No es recomendable usar excepciones genéricas, pero puede ser útil durante el desarrollo.

```python
try:
    # código riesgoso
except:
    print("Ocurrió un error desconocido.")
```

---
# 🚨 Tipos de Excepciones en Python

En Python, **las excepciones** son errores que se detectan durante la ejecución y detienen el flujo del programa si no son tratadas.

A continuación, te presentamos las **excepciones más comunes** con ejemplos para ayudarte a identificarlas y comprender cómo se producen.

---

## 🧾 1. `SyntaxError`

❌ **Error de sintaxis**: ocurre cuando el analizador detecta que el código no está correctamente escrito.

```python
print(10 / 2
```

**Salida:**

```
  File "<stdin>", line 1
    print(10/2
              ^
SyntaxError: unexpected EOF while parsing
```

🔍 Olvidamos cerrar el paréntesis. El analizador marca con una flecha dónde ocurrió el error.

---

## 🆔 2. `NameError`

❌ Se lanza cuando usas una **variable o función que no ha sido definida**.

```python
raiz = sqrt(100)
```

**Salida:**

```
NameError: name 'sqrt' is not defined
```

🔍 Falta importar `sqrt` desde el módulo `math`.

✅ Solución:

```python
from math import sqrt
raiz = sqrt(100)
```

---

## 📦 3. `IndexError`

❌ Ocurre cuando intentas acceder a una **posición inexistente** en una lista, tupla o string.

```python
lista = [1, 2, 3]
print(lista[4])
```

**Salida:**

```
IndexError: list index out of range
```

🔍 La lista tiene solo 3 elementos (índices 0 a 2), pero se intenta acceder al índice 4.

---

## 🔢 4. `TypeError`

❌ Se lanza cuando aplicas una operación entre **tipos incompatibles**.

```python
"1" + 1
```

**Salida:**

```
TypeError: can only concatenate str (not "int") to str
```

🔍 Se intentó concatenar una cadena (`"1"`) con un entero (`1`), lo cual no es válido.

✅ Solución:

```python
"1" + str(1)     # Resultado: "11"
int("1") + 1     # Resultado: 2
```

---

## 🔑 5. `KeyError`

❌ Ocurre cuando se accede a una **clave inexistente** en un diccionario.

```python
estados = {'EM': 1, 'JC': 2, 'OA': 3}
print(estados["MI"])
```

**Salida:**

```
KeyError: 'MI'
```

🔍 La clave `'MI'` no existe en el diccionario.

✅ Solución:

```python
print(estados.get("MI", "Clave no encontrada"))
```

---

## ⚠️ 6. `Warning` (Advertencias)

⚠️ Son alertas que **no interrumpen la ejecución del programa**, pero indican que algo podría causar problemas.

```python
import numpy as np

a = np.arange(5)
print(a / a)
```

**Salida:**

```
RuntimeWarning: invalid value encountered in true_divide
```

🔍 Se intentó dividir 0 por 0, generando un valor `nan` (Not a Number). El programa continúa, pero el resultado puede requerir validación posterior.

---

| Excepción           | Descripción                                    |
| ------------------- | ---------------------------------------------- |
| `ValueError`        | Conversión inválida de tipos (como int("abc")) |
| `KeyError`          | Clave no encontrada en un diccionario          |
| `IndexError`        | Índice fuera de rango en una lista o tupla     |
| `TypeError`         | Operación inapropiada entre tipos de datos     |
| `ZeroDivisionError` | División por cero                              |

---

## 🧼 Buenas prácticas

✔️ Captura solo las excepciones que esperas            
✔️ Proporciona mensajes útiles al usuario  
✔️ Usa `finally` para cerrar conexiones o archivos               
✔️ Evita `except:` sin especificar tipo (salvo para depuración)      


---
