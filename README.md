# course-r-intro


## The docker way
Create a folder for practice and `cd` to it.

```bash
mkdir ${HOME}/sandbox
```
Now, use this folder to mount a docker volume
```bash
#docker run -d -p 8787:8787 -e ROOT=TRUE -e USER=<username> -e PASSWORD=<password> --name rgeospatial -v $(pwd):/sandbox rocker/geospatial
docker run -d -p 8787:8787 -e USER=rstudio -e PASSWORD=rstudio --name rgeospatial -v $(pwd):/sandbox -w /sandbox rocker/geospatial
```
Once in Rstudio, set the working directory to `/sandbox`
```r
getwd()
setwd("/sandbox")
```
