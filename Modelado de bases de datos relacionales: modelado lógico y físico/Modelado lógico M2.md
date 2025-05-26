# 📝 Apuntes ✨
## 💾 Modulo 2: Modelo Logico🐍
---
# 🧩 Modelo Lógico de Base de Datos

## 🔷 Entidades Fuertes

Las **entidades fuertes** son aquellas que pueden existir de forma **independiente**, sin depender de ninguna otra entidad para su identificación.

### 📌 Ejemplos:

| Entidad     | Descripción                 |
| ----------- | --------------------------- |
| `CLIENTE`   | Persona que realiza pedidos |
| `EDITORIAL` | Empresa que publica libros  |

Cada entidad fuerte debe tener una **clave principal (PK)** que identifique **únicamente** a cada registro.

---

## 🔸 Entidades Débiles

Las **entidades débiles** no pueden ser identificadas únicamente por una clave propia. Dependen de una **entidad fuerte** para ser identificadas correctamente.

### 📌 Características de las Entidades Débiles:

* Utilizan una **clave parcial**, que por sí sola no es suficiente para identificar un registro.
* Esta clave parcial se **combina con una clave foránea (FK)** proveniente de la entidad fuerte para formar una **clave compuesta**.
* Se relacionan con entidades fuertes mediante **claves foráneas**.

### 📌 Ejemplos de Entidades Débiles:

| Entidad      | Depende de... | Clave Parcial    | Clave Foránea        | Atributos                                    |
| ------------ | ------------- | ---------------- | -------------------- | -------------------------------------------- |
| `PEDIDO`     | `CLIENTE`     | `cod_pedido`     | `cod_cliente (FK)`   | `fecha`, `valor`                             |
| `LIBRO`      | `EDITORIAL`   | `cod_libro`      | `cod_editorial (FK)` | `título`, `categoría`, `autor`, `ISBN`, etc. |
| `INVENTARIO` | `LIBRO`       | `cod_inventario` | `cod_libro (FK)`     | `stock`, `ubicación`, `estado`               |

---

## 🔁 Relaciones

Las **relaciones** en el modelo lógico reflejan las conexiones entre entidades. En este nivel:

* Las **entidades fuertes** y **débiles** se representan como **relaciones (tablas)**.
* Las **claves foráneas (FK)** definen cómo una tabla se vincula con otra.
* La **cardinalidad** define cuántos registros pueden estar relacionados entre sí.

### 📌 Ejemplo:

* Un `CLIENTE` puede tener **muchos** `PEDIDOS`.
* Una `EDITORIAL` puede publicar **muchos** `LIBROS`.

---

## 🧠 Modelo Lógico: Representación

El modelo lógico convierte las entidades y atributos del modelo conceptual en una representación más cercana a la estructura de una base de datos real.

### ✍️ Convenciones de Nombres:

| Elemento   | Convención                                                                        |
| ---------- | --------------------------------------------------------------------------------- |
| Relaciones | Se escriben en **MAYÚSCULAS**                                                     |
| Atributos  | Se escriben en **minúsculas**, usando `_`                                         |
| Claves     | Claves primarias y foráneas se **subrayan** o se identifican como `(PK)` o `(FK)` |

---

## 🔑 Claves Principales y Parciales

### Claves Principales (PK)

Identifican de manera **única** cada registro en una entidad fuerte.

### Claves Parciales + Foráneas (PK compuesta)

Identifican los registros de una **entidad débil**, combinando:

```text
clave_parcial + clave_foránea = clave compuesta (PK)
```

---

## 📌 Atributos Derivados

En lugar de usar atributos generales como `dirección`, es buena práctica dividirlos en atributos más **específicos**.

### 🎯 Ejemplo:

| Atributo General | Atributos Derivados                   |
| ---------------- | ------------------------------------- |
| `dirección`      | `calle`, `barrio`, `ciudad`, `estado` |

---

## ➕ Inserción de Atributos

Para añadir atributos a una entidad en tu modelo lógico, simplemente **inserta nuevas filas** en la estructura de la entidad.

### ✅ Ejemplo de Entidad en Formato Vertical:

```text
CLIENTE
--------
cod_cliente (PK)
nombre
email
telefono
calle
barrio
ciudad
estado
```

---
# 🧬 Especialización, Generalización y Atributos de Relaciones en el Modelo Conceptual

---

## 🔍 Especialización y Generalización

### 🔹 **Generalización**

Es el proceso de **agrupar entidades similares** en una entidad más general.
👉 *Ejemplo:* `persona natural` y `persona jurídica` se pueden generalizar en la entidad `cliente`.

### 🔸 **Especialización**

Es el proceso **inverso a la generalización**: consiste en **crear subtipos** a partir de una entidad general para manejar sus particularidades.
👉 *Ejemplo:* La entidad `cliente` se puede especializar en:

* `persona_natural` (con atributos como nombre, cédula, fecha de nacimiento)
* `persona_jurídica` (con atributos como razón social, NIT, representante legal)

🧠 Esto permite personalizar los atributos y relaciones según el tipo de entidad.

---

## 🧷 Atributos de Relación

Durante el modelado conceptual, **algunas relaciones pueden tener atributos propios**. Estos son llamados **atributos de relación** y su tratamiento depende de la cardinalidad de la relación.

---

### 📥 ¿Qué hacer con los atributos de relación?

Durante el desarrollo del modelo conceptual, los atributos de relación:

* En **relaciones 1:1 o 1\:N**: pueden **migrarse** a una de las entidades.
* En **relaciones N\:M**: deben **permanecer en la relación**, la cual se transforma en una **entidad asociativa**.

---

## 🔁 Migración según la Cardinalidad

### 📌 Relación 1:1

🟦 **Ambas entidades tienen una sola instancia de la relación.**
➡️ El atributo de la relación puede ser **migrado a cualquiera** de las dos entidades.

#### 🧪 Ejemplo:

**Relación:** `GESTIONA`
**Atributo:** `fecha_inicio` (cuándo comenzó el colaborador a gestionar el departamento)

| Entidad       | Relación | Entidad        |
| ------------- | -------- | -------------- |
| `COLABORADOR` | GESTIONA | `DEPARTAMENTO` |
| 1             | ---      | 1              |

🟩 **Solución:** El atributo `fecha_inicio` puede migrarse a cualquiera de las dos entidades (`colaborador` o `departamento`).

---

### 📌 Relación 1\:N

🟦 **Una entidad tiene una única ocurrencia y la otra varias.**
➡️ El atributo se migra hacia la entidad que tiene **una única instancia**.

#### 🧪 Ejemplo:

**Relación:** `TRABAJA_EN`
**Atributo:** `fecha_ingreso`

| Entidad       | Relación    | Entidad        |
| ------------- | ----------- | -------------- |
| `COLABORADOR` | TRABAJA\_EN | `DEPARTAMENTO` |
| 1             | ←           | N              |

🟩 **Solución:** El atributo `fecha_ingreso` se migra a la entidad `COLABORADOR`, ya que trabaja en un solo departamento.

---

### 📌 Relación N\:M

🟦 **Ambas entidades tienen múltiples ocurrencias.**
➡️ El atributo se mantiene en la relación, que se convierte en una **entidad asociativa**.

#### 🧪 Ejemplo:

**Relación:** `PARTICIPA_EN`
**Atributo:** `horas_trabajadas`

| Entidad       | Relación      | Entidad    |
| ------------- | ------------- | ---------- |
| `COLABORADOR` | PARTICIPA\_EN | `PROYECTO` |
| N             | ---           | M          |

🟩 **Solución:** Se crea una **nueva entidad** llamada `ASIGNACIÓN`, que contiene:

* Clave foránea de `colaborador`
* Clave foránea de `proyecto`
* Atributo `horas_trabajadas`

---

## 📋 Resumen de Reglas de Migración

| Cardinalidad | ¿Migrar atributo? | ¿A dónde migrarlo?                            |
| ------------ | ----------------- | --------------------------------------------- |
| 1:1          | ✅ Sí              | A cualquiera de las entidades                 |
| 1\:N         | ✅ Sí              | A la entidad del lado "1" (menos ocurrencias) |
| N\:M         | ❌ No              | Crear una entidad asociativa                  |

---

