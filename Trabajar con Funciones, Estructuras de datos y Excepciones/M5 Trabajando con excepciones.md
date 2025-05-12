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

## 🗂️ Tipos comunes de excepciones

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
