# 📝 Apuntes
## 💾 Modulo 4: Diagramas
---

# 🔗 Tipos de Relación en Diagramas Entidad-Relación (ER)

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

# 📌 Tipos de Cardinalidad

La **cardinalidad** describe cuántas instancias de una entidad pueden estar asociadas con instancias de otra entidad. Es clave para entender cómo se relacionan los elementos en una base de datos.

---

## 📊 Tabla de Tipos de Cardinalidad

| Tipo de Cardinalidad | Descripción                                                                 | Ejemplo                                                 |
| -------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------- |
| 1 : 1                | Una instancia de una entidad se relaciona con una sola instancia de otra.   | Un departamento es gestionado por un único colaborador. |
| 1 : N                | Una instancia de una entidad se relaciona con muchas instancias de otra.    | Un departamento tiene varios colaboradores.             |
| 0 : 1                | Una instancia puede no tener relación o solo una relación con otra entidad. | Un departamento puede no tener un colaborador asignado. |
| 0 : N                | Una instancia puede relacionarse con muchas o ninguna instancia de otra.    | Algunos departamentos no tienen colaboradores.          |
| M : N                | Muchas instancias de una entidad se relacionan con muchas de otra.          | Varios pedidos pueden incluir varios libros.            |

---

## 🔍 Explicaciones Detalladas

### ✅ 1 a 1

* Cada registro de una entidad se relaciona con uno y solo un registro de la otra entidad.
* *Ejemplo:* Un **departamento** es gestionado por **un solo colaborador**.

### 🔁 1 a N (Uno a Muchos)

* Una entidad se relaciona con varias instancias de otra.
* *Ejemplo:* Un **departamento** puede tener **muchos colaboradores**.

### ❔ 0 a 1

* Una entidad puede estar relacionada con ninguna o una sola instancia de otra.
* *Ejemplo:* Un **departamento** puede no tener **colaborador asignado**.

### 🔄 0 a N (Cero a Muchos)

* Una entidad puede tener muchas relaciones o ninguna.
* *Ejemplo:* **Varios departamentos** podrían no tener **colaboradores asignados**.

### 🔗 M a N (Muchos a Muchos)

* Muchas instancias de una entidad se relacionan con muchas de otra.
* *Ejemplo:* En un **club de libros**, varios **pedidos** pueden incluir **varios libros**.

---
