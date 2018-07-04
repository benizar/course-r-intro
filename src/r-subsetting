# Filtrando estructuras

## Vectores

Creamos el vector `vec` como ya sabemos.
```r
vec <- c(6, 1, 3, 6, 10, 5)
```

Ahora podemos acceder a sus elementos por índice, usando los corchetes (`vec[pos]`). 

**Trata de predecir** lo que harán las consultas siguientes:
```r
vec[2]
vec[c(5, 6)]
vec[-c(5,6)]
vec[vec > 5]
vec[0]
vec[-c(5,6)]
vec[c(FALSE,TRUE,FALSE,TRUE,TRUE,FALSE)]
```


## Data frames

Creamos el dataframe `df` como ya sabemos

Ahora podemos acceder a sus elementos por índice, usando los corchetes (`df[fila/s,columna/s]`). 

```r
df <- data.frame(
 name = c("John", "Paul", "George", "Ringo"),
 birth = c(1940, 1942, 1943, 1940),
 instrument = c("guitar", "bass", "guitar", "drums")
)
```

**Trata de predecir** lo que harán las consultas siguientes:
```r
df[c(2, 4), 3]
df[ , 1]
df[ , "instrument"]
df$instrument
```

Hay muchas maneras de realizar este tipo de consultas/filtros
```r
df[2,3]
df[c(2,4),c(2,3)]
df[c(2,4),3]
df[1:4, 1:2]
df[c(1,1,1,2,2), 1:3]
df[1:2, 0]
df[-c(2:4), 2:3]
df[-c(2:4),-(2:3)]
df[2]
df[1, ]
df[ ,2]
df[ ,"birth"]
df[ ,c("name","birth")]
df[c(FALSE,TRUE,TRUE,FALSE), ]
df$birth
head(df)
tail(df)
```

## Listas

Creamos una lista `lst` como ya sabemos.

Ahora podemos acceder a sus elementos por índice, usando los corchetes (`lst[id_objeto]` o `lst[[id_objeto]]`). 

```r
lst <- list(c(1, 2), TRUE, c("a", "b", "c"))
names(lst) <- c("alpha", "beta", "gamma")
```

```r
lst[c(1,2)]
lst[1]
lst[[1]]
lst$alpha
lst[[alpha]]
```
