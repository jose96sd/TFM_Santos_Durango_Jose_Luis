Esta carpeta contiene los siguientes ficheros (python notebooks):

- ETL_other_data.ipynb --> en este notebook vamos a realizar el procesamiento de los datos externos al sistema de Valenbisi 
                           con los que queremos cruzar nuestros datos de las estaciones de bicicletas.

- ETL_historico.ipynb --> en este notebook se procesan los datos históricos de Valenbici tomando un único valor por hora como 
                          referncia.

- ETL_Spark.ipynb --> procesamos los valores históricos de Valenbisi, imputando los valores medios por hora y calculando el número total de viajes por hora.

Para poder ejecutar los notebooks, se necesita realizar lo siguiente: 

- Descargar la carpeta data del siguiente enlace: https://www.dropbox.com/scl/fi/jrh7nlc7vf2k5mdletfl2/data.zip?rlkey=8rrai8rdxta1srk1vfsaqj2io&st=0nptvjq6&dl=0
- Descomprimir la carpeta data y sacar las dos carpetas que contiene: data y other_data. Guardarlos en la ruta local deseado.
- Modificar la ruta en el notebook ETL_other_data.ipynb con la ruta donde se ha guardado la carpeta other_data.
- Ejecutar el notebook ETL_other_data.ipynb. Esto generará dos ficheros: weather_conditions.txt; stations.txt
- Modificar la ruta donde se haya guardado la carpeta data (la que contiene las carpetas con los años comprimidos).
- Ejecutar el notebook ETL_historico.ipynb. Esto generará un fichero datos.txt
- Para ejecutar el notebook ETL_Spark.ipynb será necesario guardar en un servidor con Spark en la carpeta data, el fichero comprimido de 2021 (formato tar.gz). La ejecución de este notebook generará un fichero de texto data_trips.txt con los datos medios por hora, día y estación. Este fichero lo guardamos con el resto de ficheros de los otros ejecutables con el nombre data_avg.txt
