# NeoMapas-database

Las bases de datos de NeoMapas para el muestreo de invertebrados fue diseñada e implementada por JR Ferrer-Paris en un formato de base de datos relacional (SQL) y manejada a traves de una aplicación web basada en MySQL y PhP. 

Para el componente de muestreo de Aves Gustavo A. Rodríguez utilizó una base de datos en MS Access. 

Angel Solís utilizó una base de datos --- para el trabajo de identificación de escarabajos.

## Download and upload from OSF cloud

### With python
One option is using `osfclient`, a [python library and command line program](https://github.com/osfclient/osfclient):

```sh
python3 -m venv ~/workdir/venv/osf
source ~/workdir/venv/osf/bin/activate
python --version
pip install --upgrade pip
pip install osfclient
```
We can create a config file for the project, but this method require either entering the password manually for each transaction or setting an environment variable with the password value.

```sh
osf init # and provide the username (email) and project code

```

This does not seem to be a very secure and robust approach.

Also `osfclient` is not currently under active development.


### With R

Using `osfr` library in R seems to be more robust. This work with an access token, and this is kept in a local .Renviron file.


```r
library(osfr)
osf_project <- osf_retrieve_node("https://osf.io/8tuan/")
osf_ls_files(osf_project)
```




## NeoMapas Escarabajos

## NeoMapas Aves


* JR Ferrer-Paris, JP Rodríguez, AY Sánchez-Mercado (2011) Iniciativa para el Mapeo de la Biodiversidad Neotropical. Versión 1.1 en-linea. Unidad de Biodiversidad (BiodiVen), Centro de Ecologıa y Centro de Estudios Botánicos y Agroforestales del Instituto Venezolano de Investigaciones Cientıficas (IVIC), Caracas-Maracaibo, Venezuela


