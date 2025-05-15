# 📝 Apuntes
## 💾 Modulo 1: Base de Datos
---
## 🧱 Modelado de Datos: La Base de una Base de Datos Eficiente

El **modelado de datos** es un proceso fundamental al embarcarnos en un proyecto de base de datos. Durante esta etapa crucial, los datos pasan por un ciclo de:

* **Recopilación:** 📥 Se reúnen todas las piezas de información relevantes.
* **Tratamiento:** ⚙️ Los datos se limpian y preparan para su uso.
* **Estructuración:** 🏗️ Se organiza la información para crear una base sólida.

Este proceso de modelado sienta las bases para construir una **base de datos eficiente** y funcional.

### 🗺️ Los Tres Modelos Clave

Además del **modelo conceptual**, que nos ayuda a:

* **Comprender los requisitos del sistema.** 🤔
* **Explorar las estructuras y conceptos del negocio.** 🏢

También trabajamos con otros dos modelos esenciales: el **modelo lógico** y el **modelo físico**.

#### 🧠 Modelo Lógico: La Arquitectura de la Información

El **modelo lógico** se enfoca en **cómo se almacenarán los datos dentro del sistema**. Su objetivo principal es explorar los **conceptos del dominio** de la información. En este modelo, definimos los elementos fundamentales:

* **Entidades:** 📦 Los objetos o conceptos principales (ej: Cliente, Producto, Pedido).
* **Atributos:** 🏷️ Las características de las entidades (ej: Nombre del Cliente, Precio del Producto, Fecha del Pedido).
* **Claves Primarias:** 🔑 Atributos únicos que identifican cada instancia de una entidad.
* **Claves Foráneas:** 🔗 Atributos que establecen relaciones entre entidades.
* **Relaciones:** 🔗 Las conexiones entre las diferentes entidades (ej: Un Cliente *realiza* muchos Pedidos).

#### 🔩 Modelo Físico: La Implementación Concreta

Por otro lado, el **modelo físico** se centra en la **descripción de las tablas**, incluyendo:

* **Sus columnas:** 📊 La representación física de los atributos.
* **Sus relaciones:** 🔗 Cómo se implementan las conexiones entre las tablas.

A diferencia del modelo lógico, el modelo físico utiliza un **lenguaje específico para su representación**: **SQL (Structured Query Language)**, el lenguaje estándar para interactuar con **bases de datos relacionales**. 🗣️

```sql
-- Ejemplo básico en SQL para crear una tabla de Clientes
CREATE TABLE Clientes (
    ClienteID INT PRIMARY KEY,
    Nombre VARCHAR(100),
    Email VARCHAR(100)
);
```
---
