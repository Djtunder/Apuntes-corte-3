# Nombre: Kevin Nicolas Perez Tobar
# Curso: M6A
# Dinamica de Sistemas
# Clase 1: Corrección Parcial 2

## 1. Introducción
En esta clase, se hizo la retroalimentación del segundo parcial, donde se solucionaron dudas sobre la correccion, para reconcer que errores cometimos de los temas estudiados.
## 2. Resumen
La coreccion del Parcial tenia dos sistemas: uno de ellos sistemas de masa y resorte y otro que era un circuito electrico, se hizo la correccion, la retroalimentacion, y la aclaracion de dudas de los estudiantes sobre la explicacion dada por el docente.

## 🔑3. Definiciones: 

 🔑 3.1 Sistema Electrico: En Dinámica de Sistemas, un sistema eléctrico es un modelo que describe cómo variables eléctricas como voltaje, corriente o carga cambian con el tiempo, bajo la influencia de elementos como resistencias (R), inductancias (L) y capacitancias (C).

 🔑 3.2 Sistema Mecanico: En Dinámica de Sistemas, un sistema mecánico es aquel que modela el movimiento y las fuerzas que actúan sobre un cuerpo o conjunto de cuerpos. Se analiza cómo estas fuerzas generan desplazamientos, velocidades o aceleraciones en el tiempo.

## 💡4. Ejemplos 
### 4.1  Circuito RLC Serie

### Elementos del sistema:

- Fuente de voltaje: \( V(t) \)
- Resistencia: \( R \)
- Inductor: \( L \)
- Condensador: \( C \)

### 🧮 Ecuación diferencial con corriente:

$$V(t) = R \cdot i(t) + L \cdot \frac{di(t)}{dt} + \frac{1}{C} \int i(t) \, dt$$


### 🧮 Ecuación diferencial con carga:

$$L \cdot \frac{d^2q(t)}{dt^2} + R \cdot \frac{dq(t)}{dt} + \frac{1}{C} \cdot q(t) = V(t)$$

---

### 🔄 Relación entre carga y corriente:

$$i(t) = \frac{dq(t)}{dt}$$

## Ejemploo 4.2 Sistema Mecanico

###⚙️ Sistema Mecánico Traslacional (Movimiento Lineal)

### Elementos:

- **Masa** \( m \): representa la inercia del sistema.
- **Amortiguador** \( b \): resiste el movimiento proporcional a la velocidad.
- **Resorte** \( k \): almacena energía y se opone al desplazamiento.


### 🧮 Ecuación de movimiento:

$$
m \cdot \frac{d^2x(t)}{dt^2} + b \cdot \frac{dx(t)}{dt} + k \cdot x(t) = F(t)
$$

## 5. Ecuaciones

### 5.1 Ecuacion sistema masa-resorte-amortiguador 

$$m \cdot \frac{d^2x(t)}{dt^2} + b \cdot \frac{dx(t)}{dt} + k \cdot x(t) = F(t)$$

### 5.2 Ecuacion sistema Electrico

$$L \cdot \frac{d^2q(t)}{dt^2} + R \cdot \frac{dq(t)}{dt} + \frac{1}{C} \cdot q(t) = V(t)$$

## 6. Figuras

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/cd6053bfee21ec716fd542126612517e54bd406b/img/sistema%20masa-resorte.jpg" width="300">
</div>
