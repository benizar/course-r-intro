# Estructuras de datos

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

Aunque es menos habitual también podemos estructurar nuestros datos en más dimensiones.

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


## Listas

Una lista es un grupo unidimensional de objetos de R. Los elementos de una lista pueden ser cualquier objeto, incluso vectores u otras listas.

```r
lst <- list(1, "R", TRUE)
class(lst)
# "list"

list(c(1, 2), TRUE, c("a", "b", "c"))
```


## Data Frames

Un data frame es un grupo bidimensional de objetos de R. Cada columna puede tener un tipo diferente.

```r
df <- data.frame(c(1, 2, 3),
c("R","S","T"), c(TRUE, FALSE, TRUE))
class(df)
# "data.frame"
```

## Nombres (names)

Los elementos de un vector, lista o data frame pueden llevar un nombre asociado.

**Esto es muy distinto a una hoja de cálculo**.


### Nombrar al  crear el objeto

```r
nvec <- c(one = 1, two = 2, three = 3)

nvec
# one two three
#   1   2     3
```

```r
nlst <- list(one = 1, two = 2,
many = c(3, 4, 5))

nlst
# $one
# [1] 1
#
# $two
# [1] 2
#
# $many
# [1] 3 4 5
```


```r
ndf <- data.frame(numbers = c(1, 2, 3),
	letters = c("R","S","T"),
	logic = c(TRUE, FALSE, TRUE))

ndf
#    numbers letters logic
# 1        1       R  TRUE
# 2        2       S FALSE
# 3        3       T TRUE
```


### Renombrar elementos de un objeto

Los nombres también pueden ser asignados una vez creado el objeto.

```r
names(ndf)
# [1] "numbers" "letters" "logic"

names(nvec)
# [1] "one" "two" "three"

names(nvec) <- c("uno", "dos", "tres")
nvec
# uno dos tres
#   1   2    3
```

Cada estructura de datos tiene funciones que permiten algunas opciones básicas
![Helper functions for data structures](images/data-structures-helper-functions.png)


## Funciones

En R todo son objetos y llamadas a funciones

> “To understand computations in R, two slogans are helpful:
- Everything that exists is an object.
- Everything that happens is a function call."
    — John Chambers

