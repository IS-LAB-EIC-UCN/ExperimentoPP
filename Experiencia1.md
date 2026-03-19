# Experiencia 1: Meteorología

## Contexto
Una estación meteorológica registra mediciones de temperatura durante un día.  
Cada medición incluye:

- hora del registro,
- temperatura en grados Celsius.

El objetivo es desarrollar un programa que procese estos datos y entregue un resumen básico del comportamiento de la temperatura.

## Objetivo
Implementar un programa que lea un conjunto de registros meteorológicos y calcule información relevante a partir de ellos.

## Entrada
El programa debe leer un archivo de texto con el siguiente formato:

- La primera línea contiene un número entero `N`, que indica la cantidad de registros.
- Las siguientes `N` líneas contienen:
    - una hora en formato `HH:MM`
    - una temperatura decimal

## Ejemplo de entrada
```text
5
08:00 14.5
10:00 16.2
12:00 21.0
15:00 24.3
18:00 19.1
```

## Salida esperada

El programa debe mostrar:

1. La temperatura máxima registrada.
2. La temperatura mínima registrada.
3. El promedio de temperaturas.
4. La hora asociada a la temperatura máxima.
5. La hora asociada a la temperatura mínima.