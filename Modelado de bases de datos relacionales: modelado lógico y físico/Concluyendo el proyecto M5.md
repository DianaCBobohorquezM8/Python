# 📝 Apuntes ✨
## 💾 Modulo 5: Concluyendo🐍
---
# 🔗 Cómo Establecer Relaciones en Power Architect

## 📌 Tipos de Relaciones

| Tipo de Relación      | Cuándo usarla                                                                 |
| --------------------- | ----------------------------------------------------------------------------- |
| **No Identificada**   | Cuando la entidad débil ya tiene una **clave primaria o parcial** propia.     |
| **Identificada**      | Cuando la entidad débil **no tiene clave primaria propia** y depende de otra. |
| **Claves Compuestas** | En tablas asociativas que dependen de más de una entidad (ej. `items`).       |

---

## 🧭 Pasos para Crear Relaciones

### 🔷 Relaciones **No Identificadas**

**(La entidad débil tiene clave parcial o PK propia)**

1. Selecciona la tabla principal (**entidad fuerte**), por ejemplo: `CLIENTE`.
2. Haz clic en **"New Non-Identifying Relationship"** en la barra de herramientas.
3. Haz clic en la **columna PK** de la entidad fuerte, como `codigo_cliente`.
4. Conecta con la tabla relacionada, por ejemplo `PEDIDO`.

   * La **clave foránea (FK)** se creará automáticamente en la entidad débil.
   * La PK de `PEDIDO` sigue siendo independiente (ej. `numero_pedido`).

> ✅ Ejemplo:
>
> * `CLIENTE (codigo_cliente)` → `PEDIDO (codigo_cliente)`
> * `PEDIDO` tiene `numero_pedido` como PK y `codigo_cliente` como FK.

---

### 🔶 Relaciones **Identificadas**

**(La entidad débil depende de la entidad fuerte para su identificación)**

1. Selecciona la tabla principal (**entidad fuerte**), por ejemplo: `EDITORIAL`.
2. Selecciona **"New Identifying Relationship"**.
3. Haz clic en la **columna PK** de la entidad fuerte (ej. `codigo_editorial`).
4. Conecta con la tabla relacionada, como `LIBRO`.

   * La FK se agregará y **formará parte de la PK compuesta** de la tabla débil.

> ✅ Ejemplo:
>
> * `EDITORIAL (codigo_editorial)` → `LIBRO (codigo_editorial + id_libro)`
> * `LIBRO` no puede existir sin `EDITORIAL`.

---

### 🔁 Relaciones con **Claves Foráneas Compuestas**

**(Para tablas asociativas, como `ITEMS`)**

1. Selecciona la tabla `PEDIDO`, elige **"New Identifying Relationship"**.
2. Haz clic en `codigo_pedido`, conéctalo a `ITEMS`.
3. Luego selecciona la tabla `LIBRO`, elige también **"New Identifying Relationship"**.
4. Haz clic en `codigo_libro`, conéctalo a `ITEMS`.

> ✅ Resultado:
>
> * `ITEMS` tendrá una PK compuesta: `codigo_pedido + codigo_libro`.
> * Ambas claves actúan como FK también.

---

## 🔎 Otras Consideraciones

### 🔐 Claves y Roles

| Clave   | Función                                                                |
| ------- | ---------------------------------------------------------------------- |
| **PK**  | Clave primaria, identifica de forma única cada registro.               |
| **FK**  | Clave foránea, relaciona con otra tabla.                               |
| **PFK** | Clave foránea parcial (FK que también forma parte de la PK compuesta). |

### 📏 Cardinalidad

* Se asigna automáticamente al crear la relación.
* Puede ajustarse más adelante según el modelo lógico:

  * 1:1
  * 1\:N
  * 0\:N
  * etc.

---

## 🧩 Ejemplos Prácticos

### 1. Relación **Cliente - Pedido** (No identificada)

* `CLIENTE (PK: codigo_cliente)`
* `PEDIDO (PK: numero_pedido, FK: codigo_cliente)`

### 2. Relación **Libro - Inventario** (Identificada)

* `LIBRO (PK: codigo_libro)`
* `INVENTARIO (PK compuesta: codigo_libro + ubicacion)`

### 3. Tabla asociativa **Items** (Identificada con PK compuesta)

* `ITEMS (PK compuesta: codigo_pedido + codigo_libro)`
* `FKs hacia: PEDIDO y LIBRO`

---
