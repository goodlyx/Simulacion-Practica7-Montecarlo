# El Método Montecarlo

El **Método Montecarlo** es un enfoque estadístico numérico utilizado para aproximar expresiones matemáticas complejas y difíciles de evaluar mediante el uso de muestreo aleatorio y simulación computacional.

## Historia y Origen
Fue inventado por **Stanislaw Ulam** y desarrollado por **John von Neumann** en la década de 1940 durante el Proyecto Manhattan en el Laboratorio Nacional de Los Álamos. Su nombre es una referencia al Casino de Montecarlo en Mónaco, debido a que el azar y la generación de números aleatorios (como en la ruleta) son el núcleo de esta metodología.

## Definición Matemática
En términos probabilísticos, si tenemos una función f(x), el valor esperado de esta función sobre un dominio específico puede ser aproximado por la media empírica de muestras aleatorias. La ecuación fundamental de la integración Montecarlo es:

I = ∫ f(x) dx ≈ (b - a) × 1/N ∑ f(x_i)

Donde N es el número de muestras aleatorias y x_i son variables aleatorias uniformemente distribuidas en el intervalo [a, b].

## Pasos para su Implementación
1. **Definir un dominio** de posibles entradas (variables aleatorias y sus distribuciones empíricas o teóricas).
2. **Generar entradas aleatorias** a partir de una distribución de probabilidad (generalmente uniforme U(0,1) mediante generadores pseudoaleatorios).
3. **Realizar un cálculo determinista** sobre estas entradas.
4. **Agregar los resultados** de los cálculos individuales para estimar el valor final o el comportamiento estadístico del sistema.
