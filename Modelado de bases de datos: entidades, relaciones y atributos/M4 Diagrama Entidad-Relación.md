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
# 📌 Tipos de Cardinalidad en Modelado de Datos

La **cardinalidad** se refiere a la cantidad de instancias de una entidad que pueden estar asociadas con instancias de otra entidad. Este concepto es esencial para entender las relaciones entre entidades en un modelo de base de datos.

---

## 📊 Tabla Resumen de Tipos de Cardinalidad

| Tipo  | Descripción                                                                         | Ejemplo                                                                                         |
| ----- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| 1 : 1 | Una instancia de una entidad se relaciona con una sola instancia de otra entidad.   | Un estudiante tiene un único ID. Cada ID pertenece a un único estudiante.                       |
| 1 : N | Una instancia de una entidad se relaciona con múltiples instancias de otra entidad. | Un cliente puede realizar varios pedidos, pero cada pedido pertenece a un solo cliente.         |
| 0 : 1 | Una entidad puede no tener relación o tener una sola relación con otra.             | Un departamento puede no tener un colaborador asignado.                                         |
| 0 : N | Una entidad puede tener muchas relaciones o ninguna.                                | Algunos departamentos podrían no tener colaboradores asignados.                                 |
| M : N | Muchas instancias de una entidad se relacionan con muchas instancias de otra.       | Un cliente puede comprar varios productos y un producto puede ser comprado por varios clientes. |

---

## 🔍 Explicaciones Detalladas

### ✅ 1 a 1 (Uno a Uno)

* Cada registro de una entidad se relaciona con **solo uno** de otra entidad.
* 📘 *Ejemplo:* Un **estudiante** tiene un único **ID**, y cada **ID** corresponde a un solo estudiante.

---

### 🔁 1 a N (Uno a Muchos)

* Cada instancia de la entidad A se relaciona con **múltiples instancias** de la entidad B.
* Es una de las cardinalidades **más comunes** en bases de datos reales y empresariales.
* 📘 *Ejemplo:* Un **cliente** puede tener **varios pedidos**, pero **cada pedido** pertenece solo a **un cliente**.

---

### ❔ 0 a 1 (Cero o Uno)

* Una entidad puede estar relacionada con **ninguna o una sola** instancia de otra entidad.
* 📘 *Ejemplo:* Un **departamento** puede o no tener **un colaborador asignado**.

---

### 🔄 0 a N (Cero o Muchos)

* Una entidad puede estar relacionada con **muchas o ninguna** instancia de otra.
* 📘 *Ejemplo:* Puede haber **varios departamentos**, y **algunos** pueden **no tener colaboradores** asignados.

---

### 🔗 M a N (Muchos a Muchos)

* Varias instancias de una entidad pueden estar relacionadas con **varias instancias** de otra entidad.
* 📘 *Ejemplo:* Un **cliente** puede **comprar varios productos**, y un **producto** puede ser **comprado por varios clientes**.

---
