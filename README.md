# Transformaciones de Matrices en Python

Este repositorio contiene el código desarrollado en Python para realizar transformaciones de matrices, utilizando como base una matriz de píxeles cargada desde un archivo `pixeles.xlsx`. El ejercicio consiste en implementar diversas funciones que permiten aplicar transformaciones comunes en procesamiento de imágenes, como convolución, padding, stride, stacking y max pooling.

## Funciones Implementadas

### 1. Convolución (apply_convolution)
Esta función aplica una operación de convolución sobre la matriz utilizando un kernel de 3x3 para detección de bordes horizontales o verticales. La convolución es una operación fundamental en el procesamiento de imágenes, utilizada para detectar patrones como bordes o cambios de intensidad en la imagen original.

- **Argumentos:**
  - `matrix`: La matriz de píxeles original.
  - `kernel`: El kernel de 3x3 que se utilizará para detectar bordes horizontales o verticales.
  
- **Resultado:** 
  - Una matriz resultante que contiene los bordes detectados en la imagen original.

### 2. Padding (apply_padding)
Esta función agrega filas y columnas de ceros alrededor de la matriz original, incrementando así su dimensión según el número de ceros especificado por el usuario. Esta técnica es útil cuando se desea preservar el tamaño de la imagen al aplicar operaciones que reducen el tamaño de la matriz.

- **Argumentos:**
  - `matrix`: La matriz de píxeles original.
  - `padding_size`: La cantidad de filas y columnas de ceros que se deben agregar.
  
- **Resultado:** 
  - Una matriz más grande con filas y columnas de ceros agregadas.

### 3. Stride (apply_stride)
Esta función aplica un kernel de 3x3 a la matriz, similar a la convolución, pero en este caso la matriz se recorre en saltos (stride) de 2 o más posiciones. Esto permite reducir el tamaño de la matriz mientras se conservan características importantes.

- **Argumentos:**
  - `matrix`: La matriz de píxeles original.
  - `kernel`: El kernel de 3x3 que se utilizará.
  - `stride`: La magnitud del salto (stride) con el que se desplazará el kernel sobre la matriz.
  
- **Resultado:** 
  - Una matriz más pequeña generada por los saltos del kernel.

### 4. Stacking (apply_stacking)
Esta función genera múltiples mapas de características (feature maps) utilizando kernels aleatorios de 3x3. Cada mapa de características representa un patrón distinto detectado en la imagen original, simulando el comportamiento de redes neuronales convolucionales que generan múltiples vistas de una imagen.

- **Argumentos:**
  - `matrix`: La matriz de píxeles original.
  - `n`: El número de mapas de características que se desean generar.
  
- **Resultado:** 
  - Una lista de `n` mapas de características generados por los kernels aleatorios.

### 5. Max Pooling (max_pooling)
Esta función aplica un kernel de 2x2 que calcula el valor máximo en cada bloque de la matriz original. El tamaño de los saltos (stride) es configurable, lo que permite reducir el tamaño de la matriz mientras se conserva la información más importante de cada bloque.

- **Argumentos:**
  - `matrix`: La matriz de píxeles original.
  - `stride`: La magnitud del salto (stride) utilizado para recorrer la matriz.
  
- **Resultado:** 
  - Una matriz reducida donde cada valor representa el máximo de un bloque 2x2 de la matriz original.
