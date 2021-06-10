# Elevaciones-de-los-grupos-Topograficos
![image](https://user-images.githubusercontent.com/78845785/121513112-c59f1700-c9ea-11eb-951e-49127182989b.png)

![image](https://user-images.githubusercontent.com/78845785/121513065-b91abe80-c9ea-11eb-9e13-01ffed24236e.png)


library(raster)
library(rgdal)
library(mapview)

DEM <- raster("C:/Users/Usuario/Documents/Análisis de Tesis en Rstudio y SAGA GIS/Variables/Georfometria R_SAGA GIS/4 ATRIBUTOS TOPOGRAFICOS/3 atributos/DEM.tif")
plot(DEM)


Grupo1 <- raster( "C:/Users/Usuario/Documents/Análisis de Tesis en Rstudio y SAGA GIS/Grupos Topograficos/Grupo1Topografico.tif")

Grupo2 <- raster("C:/Users/Usuario/Documents/Análisis de Tesis en Rstudio y SAGA GIS/Grupos Topograficos/Grupo2Topografico.tif")
Grupo3 <- raster("C:/Users/Usuario/Documents/Análisis de Tesis en Rstudio y SAGA GIS/Grupos Topograficos/Grupo3Topografico.tif")
Grupo4 <- raster("C:/Users/Usuario/Documents/Análisis de Tesis en Rstudio y SAGA GIS/Grupos Topograficos/Grupo4Topografico.tif")

mask1Topo <- mask(DEM, Grupo1)
plot(mask1Topo)  


mask2Topo <- mask(DEM, Grupo2)
plot(mask2Topo)

mask3Topo <- mask(DEM, Grupo3)
plot(mask3Topo)

mask4Topo <- mask(DEM, Grupo4)
plot(mask4Topo)
