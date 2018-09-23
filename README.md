# course-r-intro


## The docker way
Create a folder for practice and `cd` to it.

```bash
mkdir ${HOME}/sandbox
```
Now, use this folder to mount a docker volume
```bash
docker run -d -p 8787:8787 -e USER=rstudio -e PASSWORD=rstudio --name rgeospatial -v ${HOME}/sandbox:/home/rstudio rocker/geospatial
```

