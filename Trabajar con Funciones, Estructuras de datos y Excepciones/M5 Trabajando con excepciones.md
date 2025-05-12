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
## 🧰 Características de las Excepciones Útiles para la Depuración en Ciencia de Datos

### 1. **Mensajes detallados de error**

Las excepciones en Python ofrecen **mensajes claros y específicos** sobre qué falló y por qué, lo cual permite:

* Detectar si hubo un error de tipo, clave, índice, etc.
* Ver exactamente **en qué línea** del código ocurrió el problema.

💡 *Ejemplo útil*: Si cargas un archivo con `pandas.read_csv()` y hay un error de sintaxis o falta una columna, el mensaje lo dice claramente.

---

### 2. **Trazado de pila (`Traceback`)**

El traceback muestra la **ruta completa** que siguió el código hasta llegar al error. Esto ayuda a:

* Identificar **funciones o módulos intermedios** que contribuyeron al fallo.
* Ver la **secuencia de llamadas**, útil si el código está compuesto por varias capas (funciones, clases, scripts externos, etc.).

---

### 3. **Clasificación por tipo de error**

Python clasifica las excepciones por tipo (`KeyError`, `TypeError`, `ValueError`, etc.), lo que ayuda a:

* Diagnosticar el problema rápidamente (por ejemplo, saber si se trata de un problema de tipo de dato vs. acceso inválido).
* Implementar **manejadores personalizados** según el tipo de error.

---

### 4. **Permiten mantener el flujo del programa**

Con bloques `try-except`, puedes capturar el error y:

* Continuar con el análisis sin detener el programa completo.
* Mostrar un **mensaje informativo** en lugar de un fallo técnico (mejor experiencia de usuario).
* Registrar el error en un log para análisis posterior.

---

### 5. **Apoyo para pruebas y validación**

Puedes usarlas para:

* Verificar que los datos estén en el formato esperado.
* Detectar automáticamente **valores nulos**, estructuras incompatibles o funciones mal aplicadas.
* Automatizar alertas o ajustes si el comportamiento del código no es el esperado.

---

### 6. **Depuración en entornos de producción**

En ciencia de datos aplicada (APIs, dashboards, automatizaciones), las excepciones permiten:

* Registrar errores sin interrumpir el servicio.
* Enviar alertas cuando ocurre un fallo.
* Analizar estadísticas de fallos para mejorar modelos o pipelines.

---

## 📌 Ejemplo práctico

Supón que ejecutas este código:

```python
import pandas as pd

try:
    df = pd.read_csv("ventas.csv")
    print(df["precio"].mean())
except FileNotFoundError:
    print("El archivo no se encontró. Verifica la ruta.")
except KeyError:
    print("La columna 'precio' no existe. Revisa los nombres de columna.")
```

Este fragmento:

* No interrumpe la ejecución
* Te dice **qué salió mal**
* Te ayuda a **actuar en consecuencia** (diagnóstico rápido)

---
# 🗂️ Cláusula `raise` en Python

La cláusula `raise` permite **generar excepciones personalizadas** en el código cuando una condición específica impide que el programa continúe normalmente. Es muy útil para validar entradas, controlar el flujo de ejecución y mostrar mensajes de error claros al usuario.

---

## 🔧 ¿Qué es `raise`?

`raise` es una instrucción que **lanza (genera)** una excepción intencionalmente. Al hacerlo, puedes detener la ejecución del programa o redirigirla, dependiendo de cómo manejes esa excepción con `try` y `except`.

---

## 🧠 ¿Para qué sirve?

* Detener la ejecución si se detecta un error lógico o de validación.
* Enviar mensajes personalizados sobre lo que salió mal.
* Hacer más **robustos y predecibles** tus programas.
* Integrar validaciones en funciones críticas, por ejemplo en cálculos, transformaciones o lectura de datos.

---

## 📌 Sintaxis básica

```python
raise TipoDeExcepcion("Mensaje de error")
```

### Ejemplo:

```python
raise ValueError("La lista de calificaciones no puede tener más de 4 elementos.")
```

---

## ✅ Uso práctico: Validación con `raise`

Supón que tienes una función para calcular el promedio de calificaciones. Puedes usar `raise` para asegurarte de que:

* No haya más de 4 calificaciones.
* Todos los valores sean numéricos.

```python
def calcular_promedio(calificaciones):
    if len(calificaciones) > 4:
        raise ValueError("Demasiadas calificaciones. Máximo permitido: 4")
    
    for nota in calificaciones:
        if not isinstance(nota, (int, float)):
            raise TypeError(f"Calificación inválida: {nota}. Debe ser numérica.")
    
    return sum(calificaciones) / len(calificaciones)
```

---

## 🧱 Combinar `raise` con `try` / `except`

Puedes capturar las excepciones generadas por `raise` con un bloque `try-except` para:

* Evitar que el programa se detenga.
* Mostrar mensajes de error personalizados.
* Continuar con otra acción o registrar el problema.

```python
try:
    promedio = calcular_promedio([10, 8, "9", 6])
except TypeError as e:
    print("Error de tipo:", e)
except ValueError as e:
    print("Error de valor:", e)
```

---

## 🧭 Jerarquía de Excepciones

Comprender la jerarquía ayuda a:

* Capturar errores específicos.
* Usar excepciones apropiadas en tus `raise`.

### 🔽 Resumen jerárquico (simplificado)

```text
BaseException
└── Exception
    ├── TypeError
    ├── ValueError
    ├── KeyError
    ├── IndexError
    ├── FileNotFoundError
    ├── ZeroDivisionError
    ├── ...
```

> 📌 *Importante*: Python primero detecta errores de tipo (`TypeError`) antes que errores de valor (`ValueError`), así que el orden en el `try-except` también importa.

---

## 🚨 Diferencia entre `raise` y otras excepciones

| Característica              | `raise`     | Excepciones comunes (como `KeyError`, `IndexError`) |
| --------------------------- | ----------- | --------------------------------------------------- |
| Se lanza manualmente        | ✅           | ❌ (ocurren automáticamente)                         |
| Personalizable con mensajes | ✅           | Parcialmente                                        |
| Controla validaciones       | ✅           | ❌                                                   |
| Necesita estructura `try`   | Recomendado | Opcional                                            |

---

## 🧪 ¿Por qué usar `raise` en ciencia de datos?

* Validar entradas antes de pasar a un modelo o análisis.
* Evitar errores silenciosos que dan resultados engañosos.
* Proporcionar información útil al usuario o al desarrollador.
* Aumentar la calidad del código para proyectos colaborativos.

---



