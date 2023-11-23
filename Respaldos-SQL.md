
## NeoMapas Mariposas

Todos los datos de NeoMapas Mariposas están disponibles en la base de datos SQL con el nombre `NM_Mariposas`.

Usamos el respaldo más reciente: `NeoMapas.20160605.sql` y lo colocamos en una carpeta que vamos a cargar a OSF cloud storage.

```sh
UPLOADIR=$HOME/proyectos/NeoMapas/NeoMapas-database/sandbox/sql
BCKUPDIR=$HOME/respaldo/databases/sql/
mkdir -p $UPLOADIR
mv $BCKUPDIR/NeoMapas.20160605.sql $UPLOADIR
```

Revisar otros archivos:

```sh
20110928.NMs.mysql.tar.bz2
20110202.respaldo.NME1.mysql.bz2
20110202.respaldo.NMM2.mysql.bz2
20131011.NMs.root.mysql.bz2
```

```r
library(osfr)
osf_project <- osf_retrieve_node("https://osf.io/8tuan/")
osf_ls_files(osf_project)
```

Luego usar osf_upload para cargar la carpeta con todos los archivos sql..
