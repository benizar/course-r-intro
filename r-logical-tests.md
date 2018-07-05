# Tests lógicos 

## Operadores relacionales

Dado un vector `x`
```r
x <- c(1, 2, 3, 4, 5)
```

Podemos comprobar cómo funcionan los distintos operadores lógicos disponibles en R

```r
x > 3
x >= 3
x < 3
x <= 3
x == 3
x != 3
x = 3
```

Resulta especialmente útil el operador `%in%`
```r
1 %in% c(1, 2, 3, 4)
1 %in% c(2, 3, 4)
c(3,4,5,6) %in% c(2, 3, 4)
```

## Operadores lógicos
Los operadores relacionales se pueden combinar con `&`, `|`, `xor`, `!`, `any` y `all`

Comprueba la siguiente proposición
```
x > 2 & x < 9
```
**¿Falta algo?**

Ahora comprueba todas las demás.
```r
TRUE & TRUE #TRUE
TRUE & FALSE #FALSE
FALSE & TRUE #FALSE
FALSE & FALSE #FALSE
TRUE | TRUE #TRUE
TRUE | FALSE #TRUE
FALSE | TRUE #TRUE
FALSE | FALSE #FALSE
xor(TRUE, TRUE) #FALSE
xor( TRUE, FALSE) #TRUE
xor( FALSE, TRUE) #TRUE
xor( FALSE, FALSE) #FALSE
!(TRUE) #FALSE
!(FALSE) #TRUE
any(c(TRUE, FALSE, FALSE)) #TRUE
any(c(FALSE, FALSE, FALSE)) #FALSE
all(c(TRUE, TRUE, TRUE)) #TRUE
all(c(TRUE, FALSE, TRUE)) #FALSE
```

## Filtrado lógico

La combinación de todo lo que estamos viendo puede resultar muy potente.

Volviendo al ejemplo anterior

```r
df <- data.frame(
 name = c("John", "Paul", "George", "Ringo"),
 birth = c(1940, 1942, 1943, 1940),
 instrument = c("guitar", "bass", "guitar", "drums")
)
```

¿Qué crees que hará el siguiente código?
```r
guitars <- df$instrument == "guitar"

df[guitars, ]
```

## Valores ausentes (*No data*)

En R los valores ausentes se indican con `NA`.

Los valores ausentes se propagan. Ciertas funciones como `sum()` o `mean()` tienen un argumento `na.rm` para ignorar dichos valores antes de realizar los cálculos.

```r
b <- c(1, 2, 3, 4, NA)
sum(b)
# NA

sum(b, na.rm = TRUE)
# 10
```

También podemos reemplazar los valores no deseados durante la preparación de los datos.

```r
b[is.na(b)] <- 0
```