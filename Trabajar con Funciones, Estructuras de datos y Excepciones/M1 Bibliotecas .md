Apuntes ✨ Modulo 1 Bibliotecas 🐍
---
# 🛠 **Gestión de Bibliotecas en Python con `pip`**  

## 📌 **¿Qué es `pip`?**  
`pip` es el **administrador de paquetes** de Python. Permite **instalar, actualizar y eliminar** bibliotecas de terceros en proyectos de Python.  

---

## 🔹 **Instalación de Bibliotecas**  
Para instalar una biblioteca, usa el comando:  

```python
!pip install matplotlib
```  

---

## 🔹 **Importación de Bibliotecas**  
Una vez instalada, se puede importar con:  

```python
import matplotlib
```  

También es posible **verificar la versión** instalada:  

```python
matplotlib.__version__
```  

---

## 🔹 **Manejo de Versiones**  
Para trabajar con una versión específica y evitar errores de compatibilidad:  

```python
!pip install matplotlib==3.10.1
```  

---

## 🔹 **Importación de Submódulos**  
Se pueden importar submódulos con alias para facilitar su uso:  

```python
import matplotlib.pyplot as plt
```  

---

## 🔹 **Lista de Paquetes Instalados**  
Para ver todas las bibliotecas disponibles en el entorno:  

```python
!pip list
```  

---

## 📌 **Python Package Index (PyPI)**  
`pip` funciona conectándose a **PyPI**, el repositorio central de paquetes de Python. PyPI es mantenido por la **Python Software Foundation** y permite la distribución de paquetes para que otros desarrolladores los utilicen.  

---
# 📚 **Uso de Bibliotecas en Python**  

## 📌 **Versiones de Bibliotecas**  
Las bibliotecas tienen diferentes versiones, algunas con características esenciales para proyectos específicos.  
> **Ejemplo:** La versión `1.5.0` de Pandas puede incluir funcionalidades que no están presentes en versiones más recientes o antiguas.  

---

## 🔹 **Importación de Bibliotecas**  
Las bibliotecas en Python permiten ampliar sus capacidades sin necesidad de escribir código desde cero. Se pueden importar de diferentes maneras:  

```python
import matplotlib.pyplot as plt  # Importa el módulo pyplot con alias
from matplotlib import pyplot as plt  # Otra forma de importarlo
```

📌 *Usar alias (`as plt`) facilita la escritura y mejora la legibilidad del código.*  

---

## 📊 **Creación de Gráficos con Matplotlib**  
Para generar gráficos con `Matplotlib`, se usa `plt`. Por ejemplo, para crear un gráfico de barras, primero se deben definir los datos en listas y luego utilizar `plt.bar()`.  

```python
import matplotlib.pyplot as plt

# Definir los datos
estudiantes = ["Ana", "Carlos", "Elena", "Luis"]
calificaciones = [85, 90, 78, 88]

# Crear el gráfico de barras
plt.bar(x= estudiantes ,height=notas)

# Mostrar el gráfico
plt.show()
```

Tipos de gráficos disponibles:  
- **Gráficos de líneas (`plt.plot()`)** → Útiles para visualizar tendencias.  
- **Gráficos de dispersión (`plt.scatter()`)** → Muestran relaciones entre datos.  
- **Histogramas (`plt.hist()`)** → Aplicados en análisis estadístico.  

---

## 🎲 **Selección Aleatoria con `random`**  
La biblioteca `random` permite elegir elementos aleatorios en listas o generar valores aleatorios.  

Formas de importación:  

```python
import random
from random import choice  # Importa solo la función específica
```

📌 *El método `choice()` selecciona un elemento aleatorio de una lista, mientras que `randint()` genera un número entero aleatorio dentro de un rango.*  

---

## 📖 **Uso de la Documentación**  
Consultar la documentación oficial de Python es esencial para entender las funcionalidades de las bibliotecas.  

Se puede usar la función `help()` para obtener información directamente en el entorno de Python:  

```python
help(choice)
```

📌 *La documentación explica sintaxis, funcionalidades y mejores prácticas.*  

---


