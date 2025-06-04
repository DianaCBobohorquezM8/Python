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
# 🧱 Representación de Entidades en el Modelo Físico de Bases de Datos

## 🔠 ¿Qué es VARCHAR?

`VARCHAR` es un tipo de dato utilizado para almacenar **cadenas de caracteres de longitud variable**.

* A diferencia de `CHAR` (longitud fija), `VARCHAR` **se adapta al tamaño** del texto almacenado.
* Ideal para columnas como nombres, direcciones, códigos, etc.

> 🧰 **Ejemplo ilustrativo**:
> Imagina que tienes una caja para guardar palabras:
>
> * Con `CHAR(10)`, siempre se reserva espacio para 10 caracteres, aunque uses solo 3.
> * Con `VARCHAR(10)`, solo se usa el espacio necesario para cada palabra, hasta un máximo de 10.

✅ En la tabla `CLIENTE`, usamos `VARCHAR` para columnas como:

* `nombre_cliente VARCHAR(100)`
* `direccion_cliente VARCHAR(150)`

Esto **optimiza el almacenamiento** y mejora el **rendimiento** de la base de datos.

---

## 🧩 Entidades Fuertes y Débiles

### 🔷 Entidades Fuertes

* Tienen una **clave primaria (PK)** propia.
* Pueden existir de forma independiente.
* Ejemplos: `CLIENTE`, `EDITORIAL`.

### 🔶 Entidades Débiles

* **Dependen de una entidad fuerte** para su existencia.
* No tienen PK propia, sino una **clave parcial**, que se **combina con una clave foránea (FK)**.
* Ejemplos: `PEDIDO`, `ITEMS`, `INVENTARIO`, `LIBRO`.

### 🔐 Claves

| Tipo de Clave           | Función                                                                  |
| ----------------------- | ------------------------------------------------------------------------ |
| **Clave Primaria (PK)** | Identifica de forma única un registro en una entidad fuerte.             |
| **Clave Parcial**       | Identificador parcial en entidades débiles, combinada con FK.            |
| **Clave Foránea (FK)**  | Relaciona una entidad con otra (por ejemplo, `cod_cliente` en `PEDIDO`). |

---

## 📊 Tipos de Datos en el Modelo Físico

### 📂 Principales Tipos de Datos

| Tipo de Dato   | Descripción                                    | Ejemplo de uso           |
| -------------- | ---------------------------------------------- | ------------------------ |
| `VARCHAR(n)`   | Texto variable hasta `n` caracteres            | `nombre_cliente`         |
| `CHAR(n)`      | Texto de longitud fija                         | `codigo_postal`          |
| `TEXT`         | Texto largo sin límite fijo                    | `descripcion_producto`   |
| `INTEGER`      | Números enteros                                | `cantidad`, `id_cliente` |
| `DECIMAL(p,s)` | Números decimales con precisión (`p`, `s`)     | `precio`, `descuento`    |
| `FLOAT`        | Números decimales, menos preciso que `DECIMAL` | `peso_producto`          |
| `DATE`         | Solo fecha                                     | `fecha_pedido`           |
| `BOOLEAN`      | Verdadero/Falso                                | `es_activo`              |

---

## ⚙️ Propiedades y Restricciones

* **NOT NULL**: Impide que una columna tenga valores vacíos.
* **Permitir Nulos**: En algunos campos (como promociones o regalos) se permiten valores `NULL`, por ejemplo, el precio en la tabla de libros.

---

## 🧱 Creación de Tablas

Se construyeron las siguientes tablas:

| Nombre Lógico      | Nombre Físico   | Observaciones                                       |
| ------------------ | --------------- | --------------------------------------------------- |
| `LIBRO`            | `Tb_LIBRO`      | Incluye claves parciales, campos de texto y precio. |
| `INVENTARIO`       | `Tb_INVENTARIO` | Relacionado con `LIBRO`, usa claves parciales.      |
| `Persona Natural`  | `Tb_PN`         | Subtipo de cliente.                                 |
| `Persona Jurídica` | `Tb_PJ`         | Subtipo de cliente.                                 |

🔧 Se definieron:

* Claves primarias y parciales.
* Tipos de datos para cada columna.
* Restricciones y dominio.
* Nombres **lógicos** y **físicos** para facilitar la gestión.

---

## 🔗 Relaciones y Cardinalidad

* Las **relaciones entre tablas** y su **cardinalidad** (1:1, 1\:N, N\:M) se definirán en una etapa posterior del diseño.
* La relación entre entidades fuertes y débiles depende de la presencia de claves foráneas (`FK`).

---
