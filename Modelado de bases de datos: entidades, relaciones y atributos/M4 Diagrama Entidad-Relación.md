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

