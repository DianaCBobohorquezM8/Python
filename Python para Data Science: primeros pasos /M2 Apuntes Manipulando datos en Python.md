Apuntes Modulo 2 Manipulando datos en Python
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


