# Ejemplo 2: Simulación de Inventario Estocástico

## Descripción del Problema
Una panadería desea determinar cuántos pasteles hornear diariamente para maximizar su utilidad. El costo de hornear un pastel es de $5.00 y se vende a $12.00. Los pasteles no vendidos al final del día se tiran (pérdida total). La demanda diaria es incierta, pero basándose en datos históricos, sigue esta distribución de probabilidad:

| Demanda (Pasteles) | Probabilidad P(x) | P. Acumulada | Intervalo Aleatorio |
| :---: | :---: | :---: | :---: |
| 10 | 20% (0.20) | 0.20 | 0.00 - 0.19 |
| 20 | 30% (0.30) | 0.50 | 0.20 - 0.49 |
| 30 | 40% (0.40) | 0.90 | 0.50 - 0.89 |
| 40 | 10% (0.10) | 1.00 | 0.90 - 0.99 |

## Desarrollo de la Simulación
Se asume una política fija de **hornear 25 pasteles al día**. Utilizaremos el método Montecarlo generando números aleatorios entre 0 y 1 para mapearlos a los intervalos de demanda y simular la utilidad durante 10 días.

Utilidad = (Pasteles Vendidos * $12) - (Pasteles Horneados * $5)
*Si la Demanda > Horneados, se venden solo los Horneados (Ventas Perdidas).
*Si la Demanda < Horneados, hay sobras (Pérdida por merma).

| Día | Rnd U(0,1) | Demanda Simulada | Vendidos | Sobrantes | Ventas Perdidas | Utilidad Diaria |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1 | 0.8114 | 30 | 25 | 0 | 5 | $175 |
| 2 | 0.3861 | 20 | 20 | 5 | 0 | $115 |
| 3 | 0.6637 | 30 | 25 | 0 | 5 | $175 |
| 4 | 0.8207 | 30 | 25 | 0 | 5 | $175 |
| 5 | 0.9808 | 40 | 25 | 0 | 15 | $175 |
| 6 | 0.4953 | 20 | 20 | 5 | 0 | $115 |
| 7 | 0.0370 | 10 | 10 | 15 | 0 | $-5 |
| 8 | 0.5023 | 30 | 25 | 0 | 5 | $175 |
| 9 | 0.5902 | 30 | 25 | 0 | 5 | $175 |
| 10 | 0.8697 | 30 | 25 | 0 | 5 | $175 |

**Conclusión del Ejemplo 2:** Al promediar los resultados obtenidos mediante el método Montecarlo sobre una gran cantidad de días simulados, el administrador puede evaluar si 25 pasteles es la decisión óptima o si conviene ajustar la política de producción comparándola con otros escenarios.
