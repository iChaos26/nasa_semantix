# Teste - SEMANTIX - HTTP requests to the NASA Kennedy Space Center WWW server
Estudo voltado para as requests feitas para o Space Center
Fonte oficial do dateset: http://ita.ee.lbl.gov/html/contrib/NASA-HTTP.html


#REQUIREMENTS:
Ter um ambiente linuxbrew (no caso o usado fora o Ubuntu 18.04 com um gerenciador de pacotes apache brew), com pyspark setado para Jupyter notebook. Caso nao possua nem spark nem Jupyter notebook instalados, basta seguir:

#Brew:
Clonar o Brew: git clone https://github.com/Linuxbrew/brew.git ~/.linuxbrew
Adicionar brew para o PATH: echo "export PATH='$(brew --prefix)/bin:$(brew --prefix)/sbin'":'"$PATH"' >>~/.profile
Testando instalador: $ brew install hello

#Spark:
- Java: sudo apt install scala default-jdk
- Anaconda (nao e totalmente necessario, uma vez que pode-se instalar apenas o Jupyter notebook):
-> wget https://repo.anaconda.com/archive/Anaconda3-5.3.0-Linux-x86_64.sh
-> bash Anaconda3-5.3.0-Linux-x86_64.sh
-> export PATH="$HOME/.opt/anaconda3/bin:$PATH"
- Spark: brew install apache-spark
- Jupyter: pip install jupyter
Configurando PySpark Driver:
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
export PYSPARK_PYTHON=python3
-> pip install findspark
Feito, basta rodar o init com o PATH correto do PySpark:
import findspark
findspark.init()
import pyspark
sc = pyspark.SparkContext(appName="myAppName")



