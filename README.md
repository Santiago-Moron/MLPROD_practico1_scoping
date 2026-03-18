# Práctico 1: Scoping

En el archivo "ml_prod_practico1.ipynb" encontrará los ejercicios a realizar.


## 1. Dependencias de Python

Las dependencias de Python son módulos o bibliotecas que una aplicación de Python utiliza para su correcto funcionamiento. Existen diferentes herramientas para gestionar estas dependencias, siendo las más populares `pip`, `pip-tools`, `poetry`, `uv`, entre otras.

Los prácticos son compatibles tanto con `poetry` como con `pip`, pero pueden buscar documentación de otras herramientas en su web, como por ejemplo [uv](https://github.com/astral-sh/uv) o pip-tools.


### 2.1 Instalación de poetry ***(PRIMERA OPCIÓN)***
Para instalar poetry en su sistema operativo, siga los pasos de la documentación oficial:  [poetry](https://python-poetry.org/docs/#installing-with-the-official-installer)

Tras haberlo instalado, es muy importante setear la configuración "in-project" para que se cree un entorno virtual en el directorio en donde nos encontremos, esto lo hacemos con el comando 
```bash
poetry config virtualenvs.in-project true
```


### 2.2 Uso de Poetry
Poetry nos descargará todas las dependencias necesarias para utilizar el práctico, creando un entorno virtual llamando .venv en el mismo directorio del práctico.
Para usarlo, se debe ejecutar el siguiente comando estando en el directorio del práctico (es importante estar en el mismo nivel que el archivo pyproject.toml):
```bash
poetry install
```



En cambio, si se usa pip, recomendamos crear entorno virtuales con la librería `virtualenv`.


### 3.1 Instalación de virtualenv ***(SEGUNDA OPCIÓN)***

```bash
pip install virtualenv
```

### 3.2 Creación de un entorno virtual

En Linux/Mac:
```bash
virtualenv venv -p $(which python3.11)
```

En Windows:
```bash
python -m virtualenv venv -p python3.11
```

### 3.3 Activación del entorno virtual

En Linux/Mac:
```bash
source venv/bin/activate
```

En Windows:
```bash
.\venv\Scripts\activate
```


### 3.4 Gestión con pip y PyPI

Pip es la herramienta estándar de línea de comandos que se utiliza para descargar e instalar paquetes de Python desde el Python Package Index (PyPI), el repositorio oficial de paquetes de Python.

Para gestionar dependencias con pip debe existir un archivo `requirements.txt` en el proyecto, se usa el comando `pip install -r requirements.txt` para instalar las dependencias en el entorno actual.
