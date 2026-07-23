# Ejemplo 1: Estimación de Pi (π)

## Descripción del Problema
Uno de los ejemplos clásicos del método Montecarlo es el cálculo analítico del valor de π. Imaginemos un círculo de radio r = 1 inscrito dentro de un cuadrado de lado 2r = 2. El área del círculo es πr² = π, y el área del cuadrado es (2r)² = 4.

La relación entre el área del círculo y la del cuadrado es π / 4. Si generamos coordenadas aleatorias (x, y) uniformemente distribuidas dentro del cuadrado, la probabilidad de que un punto caiga dentro del círculo es exactamente π / 4.

## Fórmula de Evaluación
Un punto (x, y) cae dentro del círculo si se cumple la inecuación pitagórica: x² + y² ≤ 1.

Estimación de π = 4 * (Número de puntos DENTRO del círculo / Número TOTAL de puntos)

## Tabla de Simulación (Primeros 10 puntos)

| Iteración | x aleatorio (U~0,1) | y aleatorio (U~0,1) | x² + y² | Resultado |
| :---: | :---: | :---: | :---: | :---: |
| 1 | 0.6394 | 0.0250 | 0.4095 | Dentro |
| 2 | 0.2750 | 0.2232 | 0.1255 | Dentro |
| 3 | 0.7365 | 0.6767 | 1.0003 | Fuera |
| 4 | 0.8922 | 0.0869 | 0.8035 | Dentro |
| 5 | 0.4219 | 0.0298 | 0.1789 | Dentro |
| 6 | 0.2186 | 0.5054 | 0.3032 | Dentro |
| 7 | 0.0265 | 0.1988 | 0.0402 | Dentro |
| 8 | 0.6499 | 0.5449 | 0.7193 | Dentro |
| 9 | 0.2204 | 0.5893 | 0.3958 | Dentro |
| 10 | 0.8094 | 0.0065 | 0.6552 | Dentro |

*(Nota: La gráfica visual generada por estos puntos se encuentra en el PDF).*
