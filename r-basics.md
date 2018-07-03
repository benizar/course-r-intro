
# Introducción a R

## Operaciones básicas

### R como calculadora

```r
5 + 5
# 10

4 - 1
# 3

1 * 2
# 2

4 ^ 2
# 16
```

### Algebra con variables

Una manera de asignar variables en R es `var <- valor` (hay otras posibilidades). Las variables creadas pueden ser reasignadas o borradas con `rm(var)`.

```r
a <- 1
b <- 2

a + b
# 3

A <- 3

a + b - A
# 0
```


Y hay otras funciones que permiten hacer cálculos mucho más complicados:

```r
round(3.1415)
# 3

factorial(3)
# 6 -- 3! = 3 x 2 x 1

sqrt(9)
# 3
```

### ¿Qué piensas que devolverá esta operación?[^1]

```r
factorial(round(2.0015) + 1)
```
[^1]: Pista: es como en Excel o en una calculadora (siempre de los paréntesis más anidados hacia los exteriores).


## Vectores

Un vector puede combinar varios elementos ordenados en un array unidimiensional. Las operaciones que apliquemos se comportan de acuerdo a la naturaleza de los vectores.

```r
vec <- c(1, 2, 3, 10, 100)
vec
# 1 2 3 10 100

vec + 4
# 5 6 7 14 104

vec * 4
# 4 8 12 40 400
!
vec * vec
# 1 4 9 100 10000

```

## Matrices

Una matriz puede combinar varios elementos en un array bidimiensional

```r
mat <- matrix(c(1, 2, 3, 4, 5, 6), nrow = 2)
mat
#      [,1] [,2] [,3]
# [1,]   1    3    5
# [2,]   2    4    6
```

```r
mat <- matrix(c(1, 2, 3, 4, 5, 6), nrow = 3)
mat
#      [,1] [,2]
# [1,]   1    3
# [2,]   2    4
# [2,]   5    6
```

Trasponer una matriz

```r
t(mat)
#      [,1] [,2] [,3]
# [1,]   1    3    5
# [2,]   2    4    6
```

## Arrays multidimensionales

Aunque es menos habitual también podemos estructurar nuestros datos en más dimensiones

```r
array(c(1, 2, 3, 4, 5, 6), dim = c(2, 2, 3))

#, , 1

#     [,1] [,2]
#[1,]    1    3
#[2,]    2    4

#, , 2

#     [,1] [,2]
#[1,]    5    1
#[2,]    6    2

#, , 3

#     [,1] [,2]
#[1,]    3    5
#[2,]    4    6
```

## Factores

## Data Frames

## Listas

## Funciones
