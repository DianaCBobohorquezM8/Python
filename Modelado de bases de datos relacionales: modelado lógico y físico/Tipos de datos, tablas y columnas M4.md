# 📝 Apuntes ✨
## 💾 Modulo 4: Tipos de datos, tablas y columnas🐍
---
# 🧠 Dominio de Datos en el Modelo Físico

El **dominio** se refiere al tipo de datos que puede contener una **columna** de una tabla en una base de datos. Esto asegura que los valores almacenados sean coherentes con su propósito.

---

## 📦 ¿Qué es un Dominio?

Un **dominio** determina:

* El **tipo de datos** permitido (texto, número, fecha, etc.).
* Las **restricciones** sobre los valores (por ejemplo, no permitir valores nulos si es clave primaria).
* La **precisión o formato** del dato.

---

## 🧮 Tipos de Datos Comunes

| Tipo de Dato      | Descripción                                                                   |
| ----------------- | ----------------------------------------------------------------------------- |
| `VARCHAR(n)`      | Cadena de texto de longitud variable. Ideal para códigos o nombres.           |
| `CHAR(n)`         | Cadena de texto de longitud fija.                                             |
| `TEXT`            | Texto largo.                                                                  |
| `INTEGER` o `INT` | Números enteros. No guarda ceros a la izquierda.                              |
| `BIGINT`          | Números enteros grandes.                                                      |
| `FLOAT`           | Números con punto decimal (precisión aproximada).                             |
| `DECIMAL(p,s)`    | Números decimales con precisión exacta (`p` total de dígitos, `s` decimales). |
| `BOOLEAN`         | Verdadero o Falso (`TRUE` o `FALSE`).                                         |
| `DATE`            | Fechas (`AAAA-MM-DD`).                                                        |
| `TIME`            | Horas (`HH:MM:SS`).                                                           |
| `TIMESTAMP`       | Fecha y hora combinadas.                                                      |
| `BLOB`            | Datos binarios (imágenes, archivos).                                          |

---

## 🔑 Clave Primaria (PK)

* Es una columna o conjunto de columnas que **identifica de forma única** cada fila en una tabla.
* No puede contener valores nulos.
* Ejemplo: `cod_cliente` puede ser de tipo `VARCHAR(10)` si incluye letras o ceros a la izquierda.

---

## 🎯 Ejemplos de Uso

| Campo             | Tipo de Dato              | Motivo                                                  |
| ----------------- | ------------------------- | ------------------------------------------------------- |
| `cod_cliente`     | `VARCHAR(10)`             | Puede tener letras y ceros a la izquierda.              |
| `precio_producto` | `FLOAT` o `DECIMAL(10,2)` | Admite decimales. `DECIMAL` es más preciso que `FLOAT`. |
| `nombre_cliente`  | `VARCHAR(100)`            | Nombre de longitud variable.                            |
| `fecha_pedido`    | `DATE`                    | Almacena solo la fecha del pedido.                      |

---

## 📚 Categorías de Tipos de Datos

### 🔢 Numéricos

* `INT`, `BIGINT`, `FLOAT`, `DECIMAL`
* Uso: precios, cantidades, IDs numéricos

### 📆 Fechas y Tiempos

* `DATE`, `TIME`, `TIMESTAMP`
* Uso: fechas de nacimiento, horarios, registro de eventos

### 🔤 Cadenas de Caracteres

* `VARCHAR`, `CHAR`, `TEXT`
* Uso: nombres, direcciones, descripciones

---

## ⚠️ Notas Importantes

* El tipo de dato puede **variar según el SGBD** (Sistema de Gestión de Base de Datos) como MySQL, PostgreSQL, Oracle, etc.
* Elegir el tipo correcto mejora el **rendimiento, integridad** y **almacenamiento** de la base de datos.

---
