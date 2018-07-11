
# Gráficos y mapas con R

Con el ánimo de entender mejor la sintaxis y las funciones disponibles vamos a explorar los siguientes ejemplos:

## Gráficos simples

- [Producing Simple Graphs with R](https://www.harding.edu/fmccown/r/). ¿Os atrevéis a crear un climograma con lo visto hasta aquí?
- [Quick-R](https://www.statmethods.net/graphs/index.html)



## Gráficos con ggplot2

- Comparación entre ggplot2 y base graphics [link](https://tutorials.iq.harvard.edu/R/Rgraphics/Rgraphics.html).
- [r-statistics.co](http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html).
- [r-graph-gallery](https://www.r-graph-gallery.com/portfolio/ggplot2-package/).

## Mapas

- [Making maps in R](https://cengel.github.io/rspatial/4_Mapping.nb.html).
- Demos con tmap ([World](https://github.com/mtennekes/tmap/tree/master/demo/WorldFacets) y [USA](https://github.com/mtennekes/tmap/tree/master/demo/USChoropleth)).
- [tmap in a nutshell](https://cran.r-project.org/web/packages/tmap/vignettes/tmap-nutshell.html#quick-thematic-map).
- [Spatial data and tmap](https://gotellilab.github.io/Bio381/StudentPresentations/SpatialDataTutorial.html).


## Mapa mudo de Tarragona con `tmap`

Vamos a descargar nuestros propios datos del Centro de Descargas del [CNIG](http://centrodedescargas.cnig.es/CentroDescargas/index.jsp#)

El fichero a descargar está dentro del apartado de Información Geográfica de Referencia:

- líneas límite (*recintos_provinciales_inspire_peninbal_etrs89.shp*).

Con estos datos, obtendríamos un `Quick Thematic Map` de la siguiente manera:

![*Quick Thematic Map* con nuestros propios datos](images/qtm-tarragona.png)

```r
# Leer un ESRI shapefile con GDAL/OGR
library(rgdal)
provincias<-readOGR(".","recintos_provinciales_inspire_peninbal_etrs89")
# Gráficos básicos de R
plot(provincias)

# Seleccionar una provincia a partir de un campo de atributos alfanuméricos
tarragona<-provincias[provincias@data$NAMEUNIT=="Tarragona", ]
plot(tarragona)

# Geometría computacional con GEOS
library(rgeos)
tgn <- gSimplify(tarragona, tol = 0.05, topologyPreserve = TRUE)
plot(tgn)

# Ajustando algunos parámetros gráficos
par(mfrow = c(1,2))
plot(tarragona,main="Original")
plot(tgn,main="Simplificado")

# tmap es una librería más avanzada para la creación de cartografía temática
par(mfrow = c(1,1))
library(tmap)
qtm(provincias, bbox = tmaptools::bb(tarragona),fill = "CODNUT1") +
  tm_layout(bg.color = "lightblue", main.title = "Tarragona en NUTs") +
  tm_text("NAMEUNIT",bg.color = "white",remove.overlap = TRUE) +
  tm_scale_bar(position = c("left", "bottom"))

# Comparar ambos polígonos
tm_shape(tarragona)+tm_borders(col = "blue") +
  tm_shape(tgn)+tm_borders(col = "red")

# También cartografía dinámica
webgis<-qtm(tarragona)
tmap_leaflet(webgis)

# Haz unas pruebas...
qtm(provincias)
prov <- gSimplify(provincias, tol = 0.05, topologyPreserve = TRUE)

catalunya<-provincias[provincias@data$NAMEUNIT=="Tarragona"|
                        provincias@data$NAMEUNIT=="Barcelona", ]
cat<-gSimplify(catalunya, tol = 0.05, topologyPreserve = TRUE)
qtm(cat)
```
