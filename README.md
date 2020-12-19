# Datos de conectividad
Todos los comandos de esta sección asumen que en cada directorio está copiado el archivo en CR05/CRTM05 (EPSG:5367) disponible en el repositorio datos-fuentes-originales.

Los comandos GDAL realizan las conversiones a Web Mercator (EPSG:3857) y WGS84 (EPSG:4326).

## Conectividad
### GAM

#### Bosque y bosque ribereño
```shell
cd gam\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.TIF
```

#### Bosque
```shell
cd gam\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE.TIF
```

#### Bosque ribereño
```shell
cd gam\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO.TIF
```

#### Migratorias
```shell
cd gam\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVDAD_MIGRATORIAS.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVDAD_MIGRATORIAS_WEB.TIF
del PROBABILIDAD_CONECTIVDAD_MIGRATORIAS.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVDAD_MIGRATORIAS_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVDAD_MIGRATORIAS.TIF
```

#### Otras
```shell
cd gam\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTROS.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTROS_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTROS.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTROS_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTROS.TIF
```

### Corredores y cantones

#### Bosque y bosque ribereño
```shell
cd corredores-cantones\bosque-bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_BRIPARIO.TIF
```

#### Bosque
```shell
cd corredores-cantones\bosque
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BOSQUE.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BOSQUE_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BOSQUE.TIF
```

#### Bosque ribereño
```shell
cd corredores-cantones\bosque-ripario
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_BRIPARIO.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_BRIPARIO_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_BRIPARIO.TIF
```

#### Migratorias
```shell
cd corredores-cantones\migratorias
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_MIGRATORIAS.TIF
```

#### Otras
```shell
cd corredores-cantones\otras
gdalwarp -t_srs EPSG:3857 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS_WEB.TIF
del PROBABILIDAD_CONECTIVIDAD_OTRAS.*
gdalwarp -t_srs EPSG:4326 -of vrt PROBABILIDAD_CONECTIVIDAD_OTRAS_WEB.TIF /vsistdout/ | gdal_translate -co compress=lzw  /vsistdin/ PROBABILIDAD_CONECTIVIDAD_OTRAS.TIF
```
