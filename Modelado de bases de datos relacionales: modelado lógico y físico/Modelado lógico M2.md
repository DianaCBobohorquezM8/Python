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

