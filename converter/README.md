### Versão do python 2.7 <br>
### Pacotes
python -m  pip install booleano <br>
python -m  pip install gdal <br>
python -m pip install shapely  <br>
<br>
Talvez  
python -m  pip install osgeo       

### Obter os shps de meso e microrregiao

### Transformar o shp da mesorregiao em map do jvectormap

#### Criar o arquivo de configuracao input_file.json
Os valores do code_field e name_field foram obtidos por uma análise do arquivo shp no QGIS
```json
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
```

#### Copiar o arquivo shp e shx para essa pasta
#### Rodar o comando python processor.py input_file.json
