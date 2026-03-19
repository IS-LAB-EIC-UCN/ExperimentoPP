# Experiencia 2: Inventario de Productos

## Contexto
Una tienda pequeña necesita revisar el stock de sus productos al final del día.  
La información del inventario está almacenada en un archivo de texto donde cada producto se describe usando varias líneas consecutivas.

El objetivo es desarrollar un programa que procese estos datos y entregue un resumen simple del inventario.

## Objetivo
Implementar un programa que lea un archivo de inventario organizado por bloques de 3 líneas y calcule información relevante a partir de sus registros.

## Entrada
El programa debe leer un archivo de texto con el siguiente formato:

- La primera línea contiene un número entero `N`, que indica la cantidad de productos.
- Luego, para cada producto, aparecen **3 líneas consecutivas**:
    1. nombre del producto,
    2. categoría,
    3. cantidad disponible en stock.

## Ejemplo de entrada
```text
5
Cuaderno
Escolar
12
Lapiz
Utiles
30
Borrador
Utiles
8
Regla
Escolar
15
Mochila
Accesorios
4
```
## Salida esperada

El programa debe mostrar:

1. El producto con mayor stock.
2. El producto con menor stock.
3. El promedio de unidades en stock.
4. La cantidad total de unidades registradas.

## Ejemplo de salida

    Producto con mayor stock: Lapiz (30)
    Producto con menor stock: Mochila (4)
    Promedio de stock: 13.8
    Total de unidades: 69
