# Tips de código para las experiencias

Este documento entrega **ayuda mínima de programación** para ambas experiencias.
Su objetivo es apoyar la lectura del archivo y el preprocesamiento de datos, **sin resolver la lógica principal del problema**.

---

## Recomendaciones generales en Python

### 1. Abrir un archivo
```python
with open("input.txt", "r", encoding="utf-8") as archivo:
    contenido = archivo.read()
    print(contenido)
```

### 2. Leer línea por línea
```python
with open("input.txt", "r", encoding="utf-8") as archivo:
    for linea in archivo:
        print(linea.strip())
```

### 3. Convertir texto a número
```python
texto = "25"
numero = int(texto)

texto_decimal = "18.7"
temperatura = float(texto_decimal)
```

### 4. Separar datos en una línea
```python
linea = "08:00 14.5"
hora, temperatura = linea.split()
temperatura = float(temperatura)
```

### 5. Guardar datos en una lista
```python
datos = []

with open("input.txt", "r", encoding="utf-8") as archivo:
    for linea in archivo:
        datos.append(linea.strip())

print(datos)
```

---

# Tips para la Experiencia 1: Meteorología

## Estructura del archivo
- La primera línea indica la cantidad de registros.
- Cada una de las siguientes líneas contiene:
    - una hora,
    - una temperatura.

Ejemplo:
```text
5
08:00 14.5
10:00 16.2
12:00 21.0
15:00 24.3
18:00 19.1
```

## Código base de lectura
```python
with open("input.txt", "r", encoding="utf-8") as archivo:
    n = int(archivo.readline().strip())

    for _ in range(n):
        linea = archivo.readline().strip()
        hora, temperatura = linea.split()
        temperatura = float(temperatura)

        print(hora, temperatura)
```

## Sugerencias
- Leer primero la cantidad de registros.
- Procesar cada línea una por una.
- Separar la hora y la temperatura con `split()`.
- Convertir la temperatura a `float`.
- Guardar cada registro si necesitan usarlo después.

## Ejemplo guardando registros
```python
registros = []

with open("input.txt", "r", encoding="utf-8") as archivo:
    n = int(archivo.readline().strip())

    for _ in range(n):
        linea = archivo.readline().strip()
        hora, temperatura = linea.split()
        temperatura = float(temperatura)

        registros.append((hora, temperatura))

print(registros)
```

---

# Tips para la Experiencia 2: Inventario de productos

## Estructura del archivo
- La primera línea indica la cantidad de productos.
- Luego, cada producto ocupa **3 líneas consecutivas**:
    1. nombre,
    2. categoría,
    3. cantidad.

Ejemplo:
```text
3
Cuaderno
Escolar
12
Lapiz
Utiles
30
Mochila
Accesorios
4
```

## Código base de lectura
```python
with open("input.txt", "r", encoding="utf-8") as archivo:
    n = int(archivo.readline().strip())

    for _ in range(n):
        nombre = archivo.readline().strip()
        categoria = archivo.readline().strip()
        cantidad = int(archivo.readline().strip())

        print(nombre, categoria, cantidad)
```

## Sugerencias
- Leer primero el número de productos.
- Luego recorrer el archivo en bloques de 3 líneas.
- Convertir la cantidad a `int`.
- Guardar cada producto en una estructura simple.

## Ejemplo guardando productos
```python
productos = []

with open("input.txt", "r", encoding="utf-8") as archivo:
    n = int(archivo.readline().strip())

    for _ in range(n):
        nombre = archivo.readline().strip()
        categoria = archivo.readline().strip()
        cantidad = int(archivo.readline().strip())

        productos.append((nombre, categoria, cantidad))

print(productos)
```

---

## Consejos finales

- Probar primero con archivos pequeños.
- Verificar que el programa lea bien la primera línea.
- Revisar que las conversiones a `int` y `float` se hagan correctamente.
- Imprimir datos intermedios durante las pruebas para detectar errores.
- Separar el problema en dos partes:
    1. leer correctamente los datos;
    2. procesarlos según lo solicitado.

