# 📝 Apuntes ✨
## 💾 Modulo 3: Modelo Físico🐍
---
# 🧱 Transición del Modelo Lógico al Modelo Físico

Al pasar del **modelo lógico** al **modelo físico**, se realiza una transformación importante en cómo se representan los datos. Esta transición implica un cambio de enfoque: de **entidades y relaciones** a **tablas y columnas**.

---

## 🔄 Cambios Clave en la Representación

| Modelo Lógico   | Modelo Físico     |
| --------------- | ----------------- |
| `Entidad`       | `Tabla`           |
| `Atributo`      | `Columna`         |
| `Relación`      | `Claves foráneas` |
| `Nombre lógico` | `Nombre físico`   |

📌 **Ejemplo**:

* Nombre lógico: `cliente`
* Nombre físico: `Tb_CLIENTE`

---

## 🛠️ Creación de Tablas en Power Architect

Power Architect es una herramienta útil para diseñar el modelo físico de una base de datos.

### ✳️ Pasos para crear una tabla:

1. Haz clic en **"nueva tabla"** o presiona la tecla **`T`** en el lienzo.
2. Asigna un **nombre físico** a la tabla, como `Tb_CLIENTE`.
3. En la sección de **columnas**, agrega cada uno de los atributos como columnas.
4. Marca una columna como **clave principal (PK)**.
5. Añade una **descripción** en el campo `Remarks` para aclarar el propósito de la tabla.

---

## 🔑 Definición de Clave Principal (PK)

La **clave principal**:

* Identifica **únicamente** cada registro en la tabla.
* No puede contener valores nulos.
* Generalmente se nombra como `cod_` seguido del nombre de la entidad.

  * Ejemplo: `cod_cliente` para la tabla `Tb_CLIENTE`.

---

## 📝 Campo "Remarks" (Descripción)

💡 Es **buena práctica** incluir una breve descripción de cada tabla en el campo **`remarks`**, para explicar:

* Qué tipo de datos contiene.
* Su propósito dentro del sistema.

✅ Esto facilita el mantenimiento y comprensión de la base de datos por parte de otros desarrolladores o analistas.

---

## 🎨 Opciones de Personalización

Aunque no se explora a fondo en esta etapa, Power Architect permite:

* Cambiar colores de las tablas.
* Personalizar bordes y líneas.
* Agrupar tablas visualmente.

Estas funciones son útiles para **mejorar la legibilidad** de modelos complejos.

---

## 📌 Resumen Visual

| Elemento                  | Detalle                                                |
| ------------------------- | ------------------------------------------------------ |
| 🧩 Entidad lógica         | Se transforma en tabla física (`Tb_ENTIDAD`)           |
| 🔢 Atributo lógico        | Se transforma en columna de la tabla                   |
| 🗝️ Clave principal (PK)  | Se define para identificar cada fila de manera única   |
| 📝 Remarks                | Se usa para documentar la función de la tabla          |
| 🎨 Personalización visual | Opcional: colores, estilos de línea, agrupación visual |

---
Claro, aquí tienes tu texto mejorado, organizado y convertido a formato Markdown con emojis para que sea más claro y fácil de entender:

---

# 🆕 Creación de Tablas en SQL Power Architect

Para diseñar una tabla en SQL Power Architect, sigue estos pasos sencillos:

1. **Crear la tabla:**

   * Haz clic en **New Table**
   * O simplemente presiona la tecla **`T`**

2. **Diseñar la tabla:**

   * Arrastra la tabla dentro del área de trabajo en la pantalla.
   * Asigna un **nombre lógico** (cómo la referencia el modelo lógico).
     *Ejemplo:* `cliente`
   * Define un **nombre físico** (cómo se implementará en la base de datos).
     *Ejemplo:* `Tb_CLIENTE`
   * Establece la **clave principal (PK)** para identificar de forma única cada registro.
---
## 🧰 Creación de una Tabla en un Proyecto de Base de Datos

Al iniciar un nuevo proyecto de base de datos, uno de los primeros pasos es crear las tablas necesarias para almacenar la información. A continuación se describen los aspectos clave en la creación de una tabla de **clientes**.

---

### 📋 1. Creación de la Tabla

* Puedes iniciar creando una tabla llamada **Clientes**.
* A esta tabla se le pueden agregar **columnas**, **claves** y otras propiedades.

---

### ➕ 2. Inserción de Columnas

* Para agregar una nueva columna, puedes:

  * Usar un **ícono de acción** en la herramienta.
  * O presionar la tecla **"c"** (atajo de teclado).
* Se abrirá un **cuadro de diálogo** donde podrás definir:

  * **Nombre lógico** (ej: Código del cliente).
  * **Nombre físico** (ej: cod\_cliente).

---

### 🔑 3. Definición de la Clave Principal

* Es fundamental definir una **clave primaria** (`Primary Key`) para identificar de manera única cada registro.
* En este caso, se establece `código_cliente` como clave principal.
* Esto implica que:

  * No puede haber **valores nulos**.
  * No puede haber **valores repetidos**.

---

### 📐 4. Selección de Tipos de Datos

Cada columna debe tener un **tipo de dato adecuado**. Por ejemplo:

| Columna         | Tipo de Dato   | Restricciones            |
| --------------- | -------------- | ------------------------ |
| código\_cliente | `VARCHAR(10)`  | Clave primaria, NOT NULL |
| nombre\_cliente | `VARCHAR(50)`  | NOT NULL                 |
| correo          | `VARCHAR(100)` |                          |

---

### 📝 5. Documentación de la Tabla

* Es recomendable añadir **comentarios** o **remarks** en cada columna.
* Esto permite a otros miembros del equipo comprender la **finalidad** de cada campo en la base de datos.

---

### ⚠️ 6. Restricciones Fundamentales

* La **clave primaria** no puede aceptar valores **nulos** (`NULL`).
* Esta es una **regla esencial** para garantizar la integridad de los datos.

---
