# 📝 Apuntes
## 💾 Modulo 3: Entidades
---
## 🧩 Definición y Clasificación de Entidades en Modelado de Datos

### 📌 ¿Qué es una Entidad?

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

* 🔷 **Rectángulos**
* 🟦 También pueden usarse **rectángulos con esquinas redondeadas**

---

### 🧱 Entidades Fuertes vs. Débiles

| Tipo de Entidad    | Descripción                                                   | Ejemplo                    | Clave                       |
| ------------------ | ------------------------------------------------------------- | -------------------------- | --------------------------- |
| **Entidad Fuerte** | Existe de forma **independiente**, no depende de otra entidad | Cliente, Producto ,Estudiante         | ✅ Tiene **clave principal** |
| **Entidad Débil**  | Depende de una **entidad fuerte** para existir                | Pedido, Descuento ,Registro de materias | 🔒 Tiene **clave parcial**  |

🔑 Una **entidad fuerte** debe tener un **atributo exclusivo** llamado **clave principal**.   
🔗 Una **entidad débil** no posee clave principal propia, sino una **clave parcial** que se **complementa con la clave principal** de la entidad fuerte asociada.

---
