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
# 🧩 Modelo Lógico de Datos

El **modelo lógico** es una representación detallada de cómo los datos serán almacenados en una base de datos. Es creado a partir del **modelo conceptual** y traduce sus descripciones a una estructura que se asemeja al diseño real de una base de datos relacional.

---

## 🔍 ¿Qué incluye el Modelo Lógico?

El modelo lógico identifica:

* 🟦 **Entidades** → Se convierten en tablas.
* 🧩 **Atributos** → Se convierten en columnas o campos.
* 🔑 **Claves primarias** → Identifican de forma única cada registro.
* 🔗 **Claves foráneas** → Establecen relaciones entre tablas.
* 🔁 **Relaciones** → Conectan entidades según reglas de negocio.

---

## 🧭 Formas de Representación del Modelo Lógico

Existen **dos formas principales** para representar el modelo lógico:

---

### 📋 Forma Vertical

* ✅ **Más común** y utilizada.
* 📐 **Visualmente parecida** a las tablas reales de una base de datos.
* 🔽 Los atributos se representan **uno debajo del otro**.
* 🔗 Las relaciones se muestran con **líneas que unen las entidades**.

#### 📌 Ejemplo (Forma Vertical):

**Entidad: Cliente**

```
Cliente
---------
ID_Cliente (PK)
Nombre
Email
Teléfono
```

**Entidad: Pedido**

```
Pedido
---------
ID_Pedido (PK)
Fecha
Valor
ID_Cliente (FK)
```

➡️ Aquí, la relación entre **Cliente** y **Pedido** se representa por una línea que conecta la clave foránea `ID_Cliente` en **Pedido** con su clave primaria en **Cliente**.

---

### 📊 Forma Horizontal

* 📏 Los atributos se colocan **uno al lado del otro**.
* 🔑 Las claves primarias se **subrayan**.
* ➡️ Las relaciones se representan con **flechas** entre tablas.
* ❌ **No se muestra la cardinalidad** de las relaciones.

#### 📌 Ejemplo (Forma Horizontal):

```
Cliente (ID_Cliente_, Nombre, Email, Teléfono)
Pedido (ID_Pedido_, Fecha, Valor, ID_Cliente ➝ Cliente)
```

---

## ✅ ¿Cuál forma utilizar?

| Forma         | Características                        | ¿Cuándo usarla?                               |
| ------------- | -------------------------------------- | --------------------------------------------- |
| 🔽 Vertical   | Más cercana al diseño de tablas reales | ✅ Recomendada para diseño y desarrollo        |
| ➡️ Horizontal | Más compacta, menos visual             | 🔍 Útil en documentación rápida o esquemática |

> 💡 Ambas representaciones son válidas. La **forma vertical** es más común ya que facilita el paso al modelo físico e implementación en un SGBD.

---


