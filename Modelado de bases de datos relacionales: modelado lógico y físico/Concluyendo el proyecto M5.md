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

# 📐 Cardinalidad en Modelado de Bases de Datos

## 🔹 ¿Qué es la Cardinalidad?

La **cardinalidad** define la **relación numérica entre instancias de dos entidades** en un modelo de base de datos. Es decir, **cuántas veces una entidad puede estar relacionada con otra**.

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

### 📏 Cardinalidad

## 🔹 ¿Por qué es Importante?

* Asegura que la base de datos **refleje correctamente las reglas de negocio**.
* Evita **datos inconsistentes o relaciones incorrectas**.
* Es clave en el diseño de modelos relacionales sólidos y eficientes.

---

## 🔹 Tipos de Cardinalidad

| Tipo     | Significado                                                               | Ejemplo                                            |
| -------- | ------------------------------------------------------------------------- | -------------------------------------------------- |
| **1:1**  | Una instancia de A se relaciona con una sola instancia de B               | Una persona tiene un único pasaporte               |
| **1\:N** | Una instancia de A se relaciona con muchas de B, pero B solo con una de A | Una editorial publica muchos libros                |
| **N:1**  | Muchas instancias de A se relacionan con una sola de B                    | Muchos empleados en un solo departamento           |
| **N\:M** | Muchas instancias de A se relacionan con muchas de B                      | Estudiantes inscritos en varios cursos y viceversa |

⚠️ **Nota**: Las relaciones N\:M se resuelven mediante una **tabla intermedia**.

<img width="256" alt="image" src="https://github.com/user-attachments/assets/cdcfc6f4-06b1-4725-b8e4-c2f3f21f0da6" />


## 🔹 Símbolos de Cardinalidad en Power Architect

| Cardinalidad | Símbolo           | Significado                         |
| ------------ | ----------------- | ----------------------------------- |
| **1**        | Número "1"        | Exactamente una instancia           |
| **0:1**      | Línea + círculo   | Cero o una (opcional)               |
| **1\:N**     | "Pata de gallina" | Una o muchas                        |
| **0\:N**     | Círculo + pata    | Cero o muchas (opcional y múltiple) |

---

## 🔹 Cómo Ajustar la Cardinalidad en Power Architect

1. **Selecciona la relación** (línea entre dos entidades).
2. **Abre propiedades** (doble clic sobre la línea).
3. **Modifica la cardinalidad** mínima y máxima en ambos extremos.
4. **Guarda los cambios** y verifica el diagrama.

---

## 🔹 🧩 Ejemplo Práctico: Relación Libro – Autor

* **Relación**: Muchos a Muchos (N\:M)
* **Solución**: Crear tabla intermedia `Libro_Autor`

| Entidad A | Relación con Tabla Intermedia | Entidad B    |
| --------- | ----------------------------- | ------------ |
| Libro     | 1\:N                          | Libro\_Autor |
| Autor     | 1\:N                          | Libro\_Autor |

---
# 🧱 Representación del Modelo Físico en Bases de Datos

## 🔹 ¿Qué es el Modelo Físico?

El **modelo físico** es la representación detallada de cómo los datos serán almacenados en un **Sistema de Gestión de Bases de Datos (SGBD)**. Se deriva del modelo lógico, pero incluye aspectos técnicos como:

* Tipos de datos exactos (INT, VARCHAR, etc.)
* Restricciones (PK, FK, NOT NULL, etc.)
* Nombres reales de tablas y columnas
* Índices, particiones y otros detalles de almacenamiento

---

## 🔹 Representación en Herramientas Comunes

### 🛠️ **SQL Power Architect**

* **Representación vertical**: Los atributos se listan uno debajo del otro.
* **PK** (Primary Key): Se marca con el símbolo **PK** al lado del campo.
* **FK** (Foreign Key): Se marca con el símbolo **FK**.
* **Relaciones**: Representadas con líneas en forma de **“pata de gallina” o tridente**, mostrando cardinalidad (1\:N, 0\:N, etc.).

### 🛠️ **MySQL Workbench**

* Similar a Power Architect, pero con íconos gráficos:

  * **Llave amarilla** 🔑 → Clave primaria (PK)
  * **Rombo anaranjado** 🔶 → Clave foránea (FK)
* Las relaciones también se representan con **patas de gallina**, visualizando la conexión entre tablas.

---

## 🔹 Alternativa: Implementación Directa en el SGBD

En lugar de sólo representar el modelo físico gráficamente, también es posible pasar directamente del modelo lógico a su **implementación en un SGBD** como:

* MySQL
* PostgreSQL
* SQL Server
* Oracle

Esto implica crear:

* Sentencias **CREATE TABLE**
* Definir **claves primarias y foráneas**
* Crear **índices, restricciones y procedimientos**

---

## 🔹 Ejemplo Simple de Representación (Power Architect o Workbench)

### Tabla: `Objetivo_Estrategico`

```
+------------------------+
| Objetivo_Estrategico   |
+------------------------+
| PK id_objetivo         |
| nombre_objetivo        |
| descripcion_objetivo   |
| periodo_ejecucion      |
+------------------------+
```

### Tabla: `Proyecto_Estrategico`

```
+----------------------------+
| Proyecto_Estrategico       |
+----------------------------+
| PK id_proyecto             |
| nombre_proyecto            |
| descripcion_proyecto       |
| cronograma                 |
| presupuesto_estimado       |
| recursos_necesarios        |
| FK id_objetivo             |
+----------------------------+
```

👉 La relación `Objetivo_Estrategico 1:N Proyecto_Estrategico` se representará gráficamente con una línea que conecta ambas tablas con símbolos de "pata de gallina".

---
