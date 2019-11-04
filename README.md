# Teste - SEMANTIX - HTTP requests to the NASA Kennedy Space Center WWW server
Análise voltada para as requests feitas para o Space Center <br>
Fonte oficial do dateset: http://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html


# Requeriments:
Ter um ambiente linuxbrew (no caso o usado fora o Ubuntu 18.04 com um gerenciador de pacotes apache brew), com pyspark setado para Jupyter notebook. <br> 
Caso não possua nem spark nem Jupyter notebook instalados, basta seguir:

## Brew:
Clonar o Brew: 
```sh
$ git clone https://github.com/Linuxbrew/brew.git  
``` 
Adicionar brew para o $PATH: 
```sh
echo "export PATH='$(brew --prefix)/bin:$(brew --prefix)/sbin'":'"$PATH"' >>~/.profile
```
## Testando instalador: 
```sh
$ brew install hello
```
## Spark:
- Java:
```sh
$ sudo apt install scala default-jdk
```
- Anaconda (não e totalmente necessário, uma vez que pode-se instalar apenas o Jupyter notebook):
```sh
-> wget https://repo.anaconda.com/archive/Anaconda3-5.3.0-Linux-x86_64.sh
 bash Anaconda3-5.3.0-Linux-x86_64.sh
 export PATH="$HOME/.opt/anaconda3/bin:$PATH"
```
- Spark
```sh
$ brew install apache-spark
```
- Jupyter: 
```sh
pip install jupyter
```
- Configurando PySpark Driver:
```sh
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
export PYSPARK_PYTHON=python3
```
- Instalando FindSpark:
```sh
pip install findspark
```
Feito, basta rodar o init com o PATH correto do PySpark:
```python
import findspark
findspark.init()
import pyspark
sc = pyspark.SparkContext(appName="myAppName")
```



