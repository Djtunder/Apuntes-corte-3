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

 Sistema Mecanico 
<div align="center">
<img src="https://github.com/Djtunder/Apuntes-Tercer-Corte/blob/cd6053bfee21ec716fd542126612517e54bd406b/img/sistema%20masa-resorte.jpg" width="300">
</div>

Sistema Electrico

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-corte-3/blob/64d3688827ad74c7f024cc5e5cdc239ab88be217/Build/CIRCUITO%20RLC.jpg" width="300">
</div>

7. Tablas

| Sistema                     | Elementos                                         | Variable de salida   | Ecuación diferencial                                                                 |
|----------------------------|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------|
| Masa-Resorte-Amortiguador  | Masa \(m\), Amortiguador \(b\), Resorte \(k\)     | Desplazamiento \(x(t)\) | $$( m \frac{d^2x(t)}{dt^2} + b \frac{dx(t)}{dt} + kx(t) = F(t)) $$                    |
| Circuito RLC Serie         | Inductancia \(L\), Resistencia \(R\), Capacitancia \(C\) | Carga \(q(t)\)    | $$( L \frac{d^2q(t)}{dt^2} + R \frac{dq(t)}{dt} + \frac{1}{C}q(t) = V(t))$$ \)          |
|                            |                                                   | Corriente \(i(t)\)     | $$( i(t) = \frac{dq(t)}{dt}) $$                                                    |

8. Ejercicio ( Parcial Resuelto)

<div align="center">
<img src="https://github.com/Djtunder/Apuntes-corte-3/blob/f41ad0526e49466acd12616d5a39cd33363bc807/img/correccion%20parcial%202.jpg" width="400">
</div>

Solución

% Parte 1: Sistema masa-resorte-amortiguador acoplado

{DCL del sistema (masa M)

$$U = F_k - F_b = 0$$

$$U = -K(y - x_1) - B(\dot{y} - \dot{x}) = 0$$

$$F_k + F_b = M\ddot{y}$$

$$K(y - x) + B(\dot{y} - \dot{x}) = M\ddot{y}$$



###  Parte 2: Circuito eléctrico

$$-e + V_L + V_{200} + V_{50} = 0$$

$$-e(t) + 2\dot{I}_1 + 200 I_1 + 50(I_1 - I_2) = 0$$

\text{Condiciones:}

$$V_{50} = V_x, \quad V_C = 0$$

$$(50(I_1 - I_2) + 200 I_2 + \frac{1}{C} \int I_2 \)$$

## 9. Codigo en Matlab

clc;
clear;

% Parámetros del circuito
L1 = 2;        % Henrios
R1 = 200;      % Ohmios
R2 = 50;       % Ohmios compartido
R3 = 20;       % Ohmios
C = 0.2;       % Faradios
e = 10;        % Voltaje constante

% Sistema de EDOs de segundo orden
% Variables de estado: i1, i2
% Representación en forma de sistema de 1er orden

f = @(t, y) [
    (1/L1)*(e - R1*y(1) - R2*(y(1) - y(2)));                          % di1/dt
    (1/(R3 + R2))*(-(1/C)*y(2) + R2/L1*(e - R1*y(1) - R2*(y(1) - y(2)))) % di2/dt
];

% Condiciones iniciales
y0 = [0; 0];   % i1(0) = 0; i2(0) = 0

% Simulación en el tiempo
tspan = [0 2];   % segundos
[t, y] = ode45(f, tspan, y0);

% Graficar la corriente del capacitor (i2)
plot(t, y(:,2), 'r', 'LineWidth', 2);
xlabel('Tiempo (s)');
ylabel('Corriente i_2(t) (A)');
title('Corriente a través del capacitor de 0.2 F');
grid on;
legend('i_2(t)');

### Grafica 






