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
print(matplotlib.__version__)
```  

---

## 🔹 **Manejo de Versiones**  
Para trabajar con una versión específica y evitar errores de compatibilidad:  

```python
!pip install matplotlib==3.8.1
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


