python 2.7
python -m  pip install booleano 
python -m  pip install gdal
python -m pip install shapely 

talvez  
python -m  pip install osgeo       

Obtem os shps de meso e microrregiao

transformar o shp da mesorregiao em map do jvectormap

criar o arquivo de configuracao input_file.json
 [{
  "name": "read_data",
  "file_name": "29ME2500G.shp"
},{
  "name": "write_data",
  "file_name": "bahia_messoregiao.js",
  "format": "jvectormap",
  "params": {
    "code_field": "geocodigo",
    "name_field": "nome",
    "name": "bahiamesorregiao"
  }
}]

copiar o arquivo shp e shx para pastar que contem o arquivo processor.js
rodar o comando python2.7 processor.py input_file.json
