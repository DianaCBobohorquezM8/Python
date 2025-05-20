# 📝 Apuntes
## 💾 Modulo 5: Atributos 
---
# 🧬 Atributos en Bases de Datos

Los **atributos** son fundamentales en el modelado de datos, ya que permiten **describir las características específicas de una entidad**. Cada atributo tiene un **tipo de dato** asociado (texto, número, fecha, etc.), lo cual facilita su almacenamiento, consulta y análisis.

---

## 📋 ¿Qué son los Atributos?

Los **atributos** son las **propiedades o características** que describen a una entidad en una base de datos.

### 🧑 Ejemplo: Entidad `Cliente`

| Atributo        | Tipo de Dato   | Descripción                    |
| --------------- | -------------- | ------------------------------ |
| Nombre          | Texto          | Nombre completo del cliente    |
| Dirección       | Texto          | Lugar de residencia o empresa  |
| Teléfono        | Número / Texto | Número de contacto             |
| Email           | Texto          | Correo electrónico del cliente |
| Tipo de persona | Texto          | Natural o jurídica             |

---

### 📚 Ejemplo: Entidad `Libro`

| Atributo           | Tipo de Dato     | Descripción                    |
| ------------------ | ---------------- | ------------------------------ |
| Título             | Texto            | Nombre del libro               |
| Autor              | Texto            | Nombre del autor o autores     |
| ISBN               | Texto / Numérico | Código internacional del libro |
| Año de publicación | Año / Fecha      | Año en que fue publicado       |
| Valor              | Numérico         | Precio del libro               |

---

## 🎯 Importancia de los Atributos

### 🔍 1. Identificación

Permiten **distinguir** entre distintas instancias de una entidad.

> Ejemplo: Dos clientes pueden llamarse igual, pero sus **números de teléfono o emails serán diferentes**.

---

### 🗃️ 2. Organización

Los atributos ayudan a **estructurar la información** de forma clara y ordenada, facilitando su almacenamiento y recuperación.

---

### 📈 3. Consulta y Análisis

Son claves para hacer **búsquedas específicas** en la base de datos.

> Ejemplo: Para encontrar todos los libros de un autor, se utiliza el atributo **`Autor`** como filtro.

---

### 🛡️ 4. Integridad de los Datos

Asignar un **tipo de dato específico** a cada atributo:

* Evita errores (por ejemplo, ingresar texto en un campo numérico).
* Asegura que los datos sean consistentes y válidos.

---

## ✅ Conclusión

Los atributos son esenciales para:

* Representar con precisión cada entidad.
* Facilitar las operaciones de búsqueda, análisis y mantenimiento de la base de datos.
* Garantizar la calidad e integridad de la información.

> 📌 **Recuerda:** Un buen diseño de atributos contribuye directamente a la **eficiencia y utilidad** de todo el sistema de información.

---
# 🧩 Tipos de Atributos en Bases de Datos

Los **atributos** describen las **propiedades o características** de una entidad. Existen diversos tipos de atributos, clasificados según su comportamiento, estructura y propósito dentro del modelo de datos.

---

## 📚 Clasificación de los Atributos

| Tipo de Atributo            | Descripción                                             | Ejemplo                                    |
| --------------------------- | ------------------------------------------------------- | ------------------------------------------ |
| 🔹 **Simple (Atómico)**     | No se puede dividir en partes más pequeñas.             | `DNI`, `Nombre`, `Código del producto`     |
| 🔸 **Compuesto**            | Puede dividirse en subatributos más específicos.        | `Dirección` → calle, ciudad, país          |
| 🔁 **Multivaluado (Multivalor)**         | Puede tener **más de un valor** para una misma entidad. | `Teléfonos`, `Correos electrónicos`        |
| 🧮 **Derivado**             | Se calcula a partir de otro atributo o entidad.         | `Edad` a partir de `Fecha de nacimiento`   |
| 🏷️ **Clave (Primary Key)** | Identifica de forma **única** a una entidad.            | `DNI`, `RUT`, `NIT`, `Código del producto` |

---

## 🔍 Tipos de Atributos en Detalle

### 🔹 Atributo Simple o Atómico

* Es **indivisible**, contiene un único valor.
* ✅ Ideal para búsquedas directas.
* 📌 *Ejemplo:* `DNI`, `Nombre`, `Precio`.

---

### 🔸 Atributo Compuesto

* Puede descomponerse en **subatributos**.
* Facilita consultas específicas por partes.
* 📌 *Ejemplo:* `Dirección` → `Calle`, `Número`, `Ciudad`, `Departamento`.

---

### 🔁 Atributo Multivaluado o Multivador

* Puede almacenar **varios valores** para una misma entidad.
* Se recomienda modelar en una **entidad separada** o usar múltiples campos.
* 📌 *Ejemplo:* `Teléfonos` de un cliente (puede tener celular y teléfono fijo).

---

### 🧮 Atributo Derivado

* Su valor se obtiene de otro atributo (no se almacena directamente).
* Aumenta la eficiencia evitando redundancia.
* 📌 *Ejemplo:* `Edad` derivada de la `Fecha de nacimiento`.

---

### 🧾 Atributo Almacenado

* El dato se guarda directamente en la base.
* Suele usarse para calcular atributos derivados.
* 📌 *Ejemplo:* `Fecha de nacimiento`, que se usa para calcular la `Edad`.

---

### 🏷️ Atributo Clave (Key Attribute)

* Se utiliza para **identificar de forma única** una instancia de entidad.
* Impide duplicidad y garantiza integridad referencial.
* 📌 *Ejemplo:* `Código del Producto`, `DNI`, `NIT`, `RUES`.

---

## 🧠 Relación entre los Atributos

* **Simples** vs **Compuestos**: Los simples no se dividen; los compuestos sí.
* **Multivaluados**: Pueden tener varios valores a diferencia de los simples.
* **Derivados**: No se almacenan, se calculan a partir de atributos **almacenados**.
* **Clave**: Se usa para diferenciar instancias de entidades en la base de datos.

---

## 📝 Ejemplo Integrador: Entidad `Cliente`

| Atributo              | Tipo         | Descripción                                   |
| --------------------- | ------------ | --------------------------------------------- |
| `DNI`                 | Clave        | Identifica de forma única al cliente          |
| `Nombre`              | Simple       | Nombre completo                               |
| `Teléfonos`           | Multivaluado | Puede tener más de un número                  |
| `Dirección`           | Compuesto    | Se divide en ciudad, calle, número, etc.      |
| `Fecha de nacimiento` | Almacenado   | Se usa para calcular la edad                  |
| `Edad`                | Derivado     | Se obtiene a partir de la fecha de nacimiento |

---

## ✅ Conclusión

* Los atributos permiten **estructurar la información** en una base de datos.
* Comprender sus tipos facilita el **diseño de modelos eficientes y escalables**.
* Una correcta clasificación ayuda a **mantener la integridad** y a **optimizar las consultas**.

---
