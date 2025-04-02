###########################################
#           DOCKERFILE                    #
#  Entorno profesional para Python 3.13   #
#  con herramientas de estructuras        #
#  de datos, entrevistas y visualización  #
###########################################

# Base de Python 3.13 (slim: Ver Ligera) IMG

FROM python:3.13-slim

# Variables de entorno para evitar errores y mejorar rendimiento
# 1- imprime print instantaneamente para debbug
# 2- Evita que python genere y sature con archivos .pyc
# 3- Establece codificiacion de lenguahje
ENV PYTHONUNBUFFERED = 1  \ 
    PYTHONDONTWRITEBYTECODE =  1 \
    LANG = C.UTF-8 


# Instalar dependencias del ssistema    
# 1- Actualizo paquetes
# 2- Instalo Graphviz
# 3- Limpia cache
RUN apt-get update && apt-get install -y \
    graphviz \
    && rm -rf /var/lib/apt/lists/* 

#instalacion de paquetes de python
RUN pip install --upgrade pip && \
    pip install \
    jupyterlab \
    pandas \
    numpy \
    matplotlib \
    seaborn \
    scikit-learn \
    ipykernel \
    ipython \
    pytest \
    rich \
    graphviz\
    pyvis \
    black \
    flake8 \
    memory-profiler


# Directorio de trabajo dentro del contendor
WORKDIR /workspace