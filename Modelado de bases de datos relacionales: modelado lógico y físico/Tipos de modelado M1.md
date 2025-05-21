# 📝 Apuntes ✨
## 💾 Modulo 1: Tipos de Modelado🐍
---
# 🧠 Modelos de Bases de Datos

Existen **diversos modelos** utilizados para diseñar, representar e implementar una base de datos. Cada modelo cumple una función específica en distintas etapas del desarrollo.

---

## 📌 1. Modelo Conceptual

* Es la **primera fase** del modelado.
* Se representa de forma **abstracta** la estructura de la base de datos.
* Utiliza diagramas **Entidad-Relación (ER)** para mostrar:

  * 🟦 **Entidades**: Objetos o conceptos clave (por ejemplo, Cliente, Producto).
  * 🔗 **Relaciones**: Conexiones entre entidades (por ejemplo, "realiza", "compra").

> ⚠️ Este modelo **no se preocupa por la implementación técnica**, solo define qué información se necesita.

---

## 📊 2. Modelo Lógico

* Traduce el modelo conceptual a un **esquema lógico**, más cercano a cómo funciona una base de datos relacional.
* Aquí:

  * Las **entidades se transforman en tablas**.
  * Se definen **atributos** (columnas o campos).
  * Se establecen **restricciones** como la **cardinalidad**.

📌 **Ejemplo de tabla lógica** para una entidad `Cliente`:

| ID\_Cliente (PK) | Nombre    | Email                                 |
| ---------------- | --------- | ------------------------------------- |
| 1                | Ana Pérez | [ana@mail.com](mailto:ana@mail.com)   |
| 2                | Luis Ríos | [luis@mail.com](mailto:luis@mail.com) |

---

## 💾 3. Modelo Físico

* Es la **fase de implementación real** en un sistema gestor de bases de datos (SGBD), como **MySQL, PostgreSQL, Oracle, etc.**
* Se definen detalles técnicos como:

  * Tipos de datos (`VARCHAR`, `INT`, `DATE`...).
  * Si un campo **permite valores nulos**.
  * Claves primarias y foráneas.
  * Índices y optimizaciones.

🛠️ Herramientas como **SQL Power Architect** o **MySQL Workbench** pueden ayudarte a construir el modelo físico.

---

## 🔁 Cardinalidad

La **cardinalidad** define **cuántas veces** una entidad puede estar relacionada con otra. Se expresa como un **mínimo y máximo**.

| Ejemplo | Descripción                                             |
| ------- | ------------------------------------------------------- |
| 1\:N    | Un cliente puede hacer muchos pedidos.                  |
| N\:M    | Un estudiante puede estar en varios cursos y viceversa. |

---

## 🔗 Relaciones

* En el **modelo lógico**, las **relaciones del modelo conceptual** se transforman en tablas o conexiones entre tablas mediante **claves foráneas**.
* Permiten mantener **consistencia e integridad** en los datos.

---

## 🧱 Restricciones

Las restricciones aseguran la **integridad de la base de datos**. Algunas comunes son:

| Tipo de Restricción   | Descripción                                       |
| --------------------- | ------------------------------------------------- |
| 🔑 Unicidad (PK)      | Evita registros duplicados.                       |
| ❌ Not Null            | El campo no puede quedar vacío.                   |
| 🔗 Clave foránea (FK) | Establece relaciones con otras tablas.            |
| 🔍 Check              | Valida que los datos cumplan ciertas condiciones. |

---


