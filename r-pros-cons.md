# Razones para aprender R

Existen otras herramientas que facilitan el análisis de datos de todo tipo (Excel, Tableau, PowerBI, Matlab, etc). Evidentemente cada herramienta tiene sus pros y contras por lo que hay que decidir sobre su uso teniendo en cuenta el máximo número de características, evitando al mismo tiempo malgastar esfuerzos con la herramienta equivocada. Los siguientes motivos 

## Características de R

Según un estudio realizado por [DS4B](http://www.business-science.io/business/2017/12/27/six-reasons-to-use-R-for-business.html#appendix-1) R posee una combinación ideal de las características siguientes:

- Capacidades (1 = bajas, 10 = altas). Gran potencial, multiplataforma, colaborativo (*papers*), etc
- Facilidad de aprendizaje (1 = difícil, 10 = fácil)
- Coste (gratuito/mínimo, bajo, elevado)
- Tendencias de uso (0 = En retroceso, 5 = estable, 10 = En crecimiento)

![[source: buisiness-science.io](http://www.business-science.io/assets/ds4b_rating.png)](images/ds4b_rating.png)

Finalmente, cuando se habla de curvas de aprendizaje y/o curvas de experiencia, hay que recordar la existencia de **[discontinuidades en la curva de aprendizaje](https://en.wikipedia.org/wiki/Experience_curve_effects)**.

## R vs Python

- Python para informáticos/ingenieros
- R para científicos y analistas

## Facilidad de aprendizaje

El aprendizaje de R para data science se ha visto muy facilitado por el `Tidyverse`. En los últimos años se están desarrollando muchas librerías como `dplyr` o `ggplot2` que proporcionan una manera consistente y estructurada para trabajar con datos de todo tipo. Esto hace que la mencionada curva de aprendizaje sea cada vez menos pronunciada para tareas relativamente complejas.

Existen numerosos recursos online para aprender a realizar casi cualquier tarea con R. Para este curso recomendamos los siguientes **tutoriales**:

- [A (very) short introduction to R (2017)](docs/a-very-short-introduction-to-r.pdf)
- [An Introduction to R (2018)](docs/r-intro.pdf)
- Rstudio's R language introduction ([primera parte](docs/r-language-1.pdf) y [segunda parte](docs/r-language-2.pdf))
- ...

Y las siguientes ***cheat sheets***:

- [Base R](docs/base-r-cheat-sheet.pdf)
- [RStudio's IDE](docs/rstudio-ide-cheat-sheet.pdf)
- [Importación de datos](docs/r-data-import-cheat-sheet.pdf)
- [Visualización](docs/r-data-visualization-cheat-sheet.pdf)
- [Rmarkdown](docs/rmarkdown-cheat-sheet.pdf)
- ...

Evidentemente, también hay **manuales y libros** que recogen toda esta información (y mucho más):

- [R in Action](https://www.manning.com/books/r-in-action-second-edition?a_bid=5c2b1e1d&a_aid=RiA2ed)
- [R in 24 Hours, Sams Teach Yourself](https://www.amazon.com/24-Hours-Sams-Teach-Yourself/dp/0672338483)
- [R for Everyone](https://www.amazon.com/Everyone-Advanced-Analytics-Graphics-Addison-Wesley/dp/013454692X/)
- ...

## Generación de informes con R

R destaca por su capacidad de crear informes y aplicaciones con mayor eficiencia que otras plataformas. Esto se puede sintetizar en el uso de [Rmarkdown](https://rmarkdown.rstudio.com/lesson-14.html) para la generación de **informes** y [Shiny](http://shiny.rstudio.com/) para la creación de **aplicaciones web interactivas**.

<iframe id="example1" src="https://gallery.shinyapps.io/goog-trend-index/" style="border: none; width: 100%; height: 850px" frameborder="0"></iframe>


## Comunidad R

### Librerías compartidas

Desde sus orígenes, ha resultado muy sencillo acceder a una gran cantidad de librerías de código proporcionadas por la comunidad. Existen más de 14.000 librerías (*packages*) que cubren todo tipo de necesidades, desde el *deep learning* hasta la creación de gráficos o mapas. Estas librerías pueden ser consultadas por temáticas en el [Task View](https://cran.r-project.org/web/views/).

Otras librerías menos conocidas también pueden ser consultadas en repositorios de código de los desarrolladores (ver Github o Bitbucket).


### Webs especializadas/social

- [R-Bloggers](https://www.r-bloggers.com/)
- [The R graph gallery](https://www.r-graph-gallery.com/)
- ...
