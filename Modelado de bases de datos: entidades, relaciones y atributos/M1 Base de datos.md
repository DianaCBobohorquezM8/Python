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
## 💾 Sistemas de Gestión de Bases de Datos (SGBD)

Un **Sistema de Gestión de Bases de Datos (SGBD)** es la **interfaz clave** 🔑 que nos permite interactuar y trabajar con una base de datos. A través del SGBD, podemos realizar diversas acciones esenciales:

* **Alterar:** 🛠️ Modificar la estructura o los datos existentes.
* **Excluir:** 🗑️ Eliminar datos o elementos de la base de datos.
* **Incluir:** ➕ Agregar nuevos datos o elementos a la base de datos.
* **Consultar:** 🔍 Recuperar información específica de la base de datos.

### ❗ Diferenciando la Base de Datos del SGBD

Es **crucial** comprender la distinción entre la **base de datos** en sí y el **SGBD**. Cuando escuchamos nombres como **MySQL**, **Oracle**, o **SQL Server**, estamos hablando de **SGBDs**. Estos son softwares especializados diseñados para **gestionar** las bases de datos de manera eficiente. ⚙️

### 📌 La Importancia Fundamental de una Base de Datos

Se destaca la **necesidad imperante** de contar con un **registro organizado de información**. 📚 Piensa en ejemplos cotidianos:

* **Bibliotecas:** 🏢 Necesitan organizar sus libros para facilitar la búsqueda y el préstamo.
* **Supermercados:** 🛒 Deben gestionar su inventario, precios y ventas de manera estructurada.
* **Empresas de Ecommerce:** 🛍️ Requieren un registro detallado de productos, clientes, pedidos y envíos para operar eficientemente y mantener el contacto con sus clientes. 📧

Una base de datos bien organizada **simplifica la gestión** y **optimiza la interacción** con los clientes.

### 🗣️ Niveles de Lenguajes de Programación en el Contexto de Bases de Datos

Se identifican dos niveles principales de lenguajes:

* **Alto Nivel:** 🗣️ Este nivel se asemeja al **lenguaje cotidiano** y está estrechamente relacionado con el **modelado conceptual**. Es más abstracto y fácil de entender para los humanos.

* **Bajo Nivel:** 💻 Este nivel se acerca al **lenguaje de máquina**, que es el idioma que los **computadores** comprenden directamente. Es más técnico y específico para la arquitectura del hardware.

  ### 🗣️ Lenguajes de Alto y Bajo Nivel: Una Comparación

* **Alto Nivel:** Se asemeja al **lenguaje humano**. Es más intuitivo y fácil de entender para nosotros.
* **Bajo Nivel:** Se acerca al **lenguaje de la máquina**. Es el idioma que los computadores comprenden directamente.

#### 🗺️ Ejemplos en el Modelado de Bases de Datos

* **Modelo Conceptual:** Se considera un modelo de **alto nivel**.
* **Modelos Físicos:** Se consideran modelos de **bajo nivel**.
---
