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

# 🧱 Pasos para Construir el Modelo Lógico de Datos (MLD)

El proceso de **modelado de una base de datos** no comienza directamente con el modelo lógico. Existen varias etapas previas que garantizan que el modelo final cumpla con todos los requisitos del usuario.

---

## 🔄 Etapas del Proceso de Modelado

| Paso                              | Descripción                                                                                                    |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| 1️⃣ **Entrevista con el usuario** | Se recopilan los requerimientos, reglas de negocio y necesidades.                                              |
| 2️⃣ **Creación del Mini Mundo**   | Se define un subconjunto del mundo real que será representado en la base de datos.                             |
| 3️⃣ **Modelo Conceptual**         | Se construye utilizando diagramas entidad-relación para representar entidades y relaciones de forma abstracta. |
| 4️⃣ **Modelo Lógico**             | Se transforma el modelo conceptual en una estructura lógica (relaciones, claves, tipos de datos).              |
| 5️⃣ **Modelo Físico**             | Se implementa el modelo lógico en un sistema gestor de base de datos (SGBD) específico.                        |

---

## 🔁 Transición al Modelo Lógico

Una vez definido el **modelo entidad-relación (ER)**, se realiza la **transición al Modelo Lógico de Datos (MLD)**:

* 🔁 Se convierten **entidades** en **relaciones**.
* 🔗 Se definen **claves primarias** y **foráneas**.
* 🧩 Se estructuran los **atributos** de cada relación.
* 📊 Se representan las **restricciones y cardinalidades**.

---

## 🛠️ Herramienta Recomendada: diagrams.net

* Puedes usar **[diagrams.net](https://diagrams.net)** (antes draw\.io) para crear el modelo lógico visualmente.
* Esta herramienta te permite trabajar de forma colaborativa, guardar en la nube y exportar en varios formatos.

---

## 📌 Diferencias entre Modelo Lógico y Modelo Físico

| Concepto       | Modelo Lógico 🧩        | Modelo Físico 💾                 |
| -------------- | ----------------------- | -------------------------------- |
| Representación | Relaciones              | Tablas en una base de datos      |
| Enfoque        | Estructura lógica       | Implementación técnica           |
| Claves         | Primarias y foráneas    | Tipos de datos, índices, etc.    |
| Herramientas   | diagrams.net, ERD tools | SQL, DBMS como MySQL, PostgreSQL |

---


