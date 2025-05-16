# 📝 Apuntes
## 💾 Modulo 3: Entidades
---
## 🧩 Definición y Clasificación de Entidades en Modelado de Datos

### 📌 ¿Qué es una Entidad?
Una entidad es un objeto o concepto que tiene existencia propia dentro del sistema que estamos modelando.
Se identifican normalmente como sustantivos (cosas, personas, lugares, conceptos).   
Una **entidad** es un **objeto único** del mundo real que puede representar cosas **concretas** o **abstractas**.    
🔍 Por ejemplo:
* **Clientes**
* **Empresa**

---

### 🔍 Identificación de Entidades

Para saber si algo puede considerarse una entidad, se puede usar un **artículo definido o indefinido**:

| Tipo de artículo | Ejemplo     | ¿Es una entidad? |
| ---------------- | ----------- | ---------------- |
| El / La          | El cliente  | ✅ Sí             |
| Un / Una         | Una empresa | ✅ Sí             |

---

### 🧱 Tipos de Entidades

| Tipo de Entidad | Descripción               | Ejemplo      | 
| --------------- | ------------------------- | ------------ |
| **Tangible**    | Puede tocarse físicamente | Carro     🚗   |
| **Abstracta**   | No tiene forma física     | Departamento 🏢|

---

### 📐 Representación Gráfica

Las entidades se representan en los **Diagramas Entidad-Relación (ER)** mediante:

* 🟦 **Rectángulos**
* 🟦 También pueden usarse **rectángulos con esquinas redondeadas**

---

### 🧱 Entidades Fuertes vs. Débiles

| Tipo de Entidad    | Descripción                                                   | Ejemplo                    | Clave                       |
| ------------------ | ------------------------------------------------------------- | -------------------------- | --------------------------- |
| **Entidad Fuerte** | Existe de forma **independiente**, no depende de otra entidad | Cliente, Producto ,Estudiante         | ✅ Tiene **clave principal** |
| **Entidad Débil**  | Depende de una **entidad fuerte** para existir                | Pedido, Descuento ,Registro de materias | 🔒 Tiene **clave parcial**  |

🔑 Una **entidad fuerte** debe tener un **atributo exclusivo** llamado **clave principal**.   
🔗 Una **entidad débil** no posee clave principal propia, sino una **clave parcial** que se **complementa con la clave principal** de la entidad fuerte asociada.

### 🧠 ¿Cómo identificar una entidad?

Para detectar **entidades** en un texto o problema, busca **sustantivos clave** que representen **objetos del mundo real** o **conceptos del sistema**.

Por ejemplo, en una plataforma de **e-commerce**, podríamos identificar:

* 🧍 **Cliente**
* 📚 **Libro**
* 🏢 **Editorial**
* 🧾 **Pedido de compra**
* 📦 **Inventario**

---

### 🧬 Información Asociada (Atributos)

Cada entidad puede tener **atributos** que describen sus características.

| 🧩 Entidad  | 🏷️ Atributos posibles      |
| ----------- | --------------------------- |
| **Libro**   | Título, Autor, ISBN, Precio |
| **Cliente** | Nombre, Correo, Dirección   |
| **Pedido**  | Fecha, Monto total, Estado  |

---

### ⚖️ Reglas de Negocio

Las **reglas de negocio** definen **restricciones o condiciones** que afectan a las entidades y sus relaciones.

📌 **Ejemplo:**

> ❌ *"Un libro no puede ser provisto por varias editoriales."*
> ✅ Esto implica una **relación 1:1** entre **Libro** y **Editorial**.

---

## 🔗 Tipos de Relación en Diagramas Entidad-Relación (ER)

### 🧩 ¿Qué es una Relación?

Una **relación** representa la **conexión entre dos o más entidades**.
En un **diagrama entidad-relación**, se representa mediante un **rombo** (🔷).

---

### 🔄 Tipos de Relaciones según la cantidad de entidades

| Tipo de Relación | Descripción                       | Ejemplo                           |
| ---------------- | --------------------------------- | --------------------------------- |
| 🔸 **Binaria**   | Conecta **dos** entidades         | Cliente ◊ Pedido                  |
| 🔺 **Ternaria**  | Conecta **tres** entidades        | Médico ◊ Paciente ◊ Tratamiento   |
| 🔷 **N-aria**    | Conecta **más de tres** entidades | Proyecto ◊ Empleado ◊ Rol ◊ Fecha |

---

### 📏 Cardinalidad

La **cardinalidad** describe **cuántas instancias** de una entidad pueden estar asociadas con instancias de otra entidad dentro de una relación.

🔑 Es **esencial** para entender la naturaleza de la relación entre entidades.
Por ejemplo:

* **1:1 (Uno a uno)** → Un país tiene un solo presidente.
* **1\:N (Uno a muchos)** → Un cliente puede hacer muchos pedidos.
* **N\:M (Muchos a muchos)** → Un estudiante puede inscribirse en varios cursos, y un curso puede tener varios estudiantes.

---

