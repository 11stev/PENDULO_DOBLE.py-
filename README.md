# PENDULO_DOBLE.py-
Proyecto 1
<h1 style="color: red;">Péndulo Doble - Simulación en Python</h1>

##  Introducción
El **péndulo doble** es un sistema físico que consiste en dos péndulos acoplados, uno suspendido del otro. 
Este sistema es un ejemplo clásico de un sistema **dinámico no lineal** y exhibe un comportamiento **caótico** dependiendo de sus condiciones iniciales.

En este proyecto, hemos implementado una simulación del **péndulo doble** en Python utilizando **POO (Programación Orientada a Objetos)** y principios de la mecánica clásica.

---

<h2 style="color: red;"> Características del Proyecto</h2>

- Implementación basada en **Programación Orientada a Objetos**.
- Uso de **métodos y propiedades** con `@property` para una mejor gestión de los parámetros.
- Simulación utilizando **ecuaciones de Lagrange**.
- Visualización gráfica del movimiento del péndulo doble.

---

<h2 style="color: red;"> Estructura del Código</h2>

```bash
 pendulo_doble/
│--  main.py          # Archivo principal de ejecución
│--  pendulo.py       # Clase que define el Péndulo Doble
│--  README.md        # Documentación del proyecto
```

---

<h2 style="color: red;"> Instalación</h2>

Para ejecutar este proyecto en tu máquina, sigue estos pasos:

```bash
# Clona el repositorio (si lo tienes en GitHub)
git clone https://github.com/tu_usuario/pendulo_doble.git
cd pendulo_doble

# Instala las dependencias necesarias
pip install numpy matplotlib

# Ejecuta la simulación
python main.py
```

---

<h2 style="color: red;"> Explicación del Código</h2>

###  `__init__(self, ...)`
El método `__init__` inicializa las variables del sistema:
```python
def __init__(self, g, m1, m2, t1, t2, w1, w2, L1, L2):
    self.g = g    # Gravedad
    self.m1 = m1  # Masa del primer péndulo
    self.m2 = m2  # Masa del segundo péndulo
    self.t1 = t1  # Ángulo del primer péndulo
    self.t2 = t2  # Ángulo del segundo péndulo
    self.w1 = w1  # Velocidad angular del primer péndulo
    self.w2 = w2  # Velocidad angular del segundo péndulo
    self.L1 = L1  # Longitud del primer péndulo
    self.L2 = L2  # Longitud del segundo péndulo
```

###  `@property` y `@setter`
Estos decoradores se usan para **controlar y validar** los valores de los parámetros:
```python
@property
def g(self):
    return self._g

@g.setter
def g(self, valor):
    if valor > 0:
        self._g = valor
    else:
        raise ValueError("La gravedad debe ser positiva.")
```

---

<h2 style="color: red;"> Visualización</h2>

Este proyecto genera una simulación animada del péndulo doble utilizando `matplotlib`.

Ejemplo de gráfica:

![Ejemplo de simulación](https://upload.wikimedia.org/wikipedia/commons/5/5f/Doble_pendulo_animacion.gif)

---

<h2 style="color: red;"> Contribuciones</h2>
Si deseas mejorar este proyecto, ¡las contribuciones son bienvenidas! Puedes hacer un **fork** y enviar un **pull request**. 

---

<h2 style="color: red;"> Licencia</h2>
Este proyecto está bajo la licencia **MIT**. Puedes usarlo y modificarlo libremente.

---

** Autor:** *Johans steven Hernandez Diaz*

