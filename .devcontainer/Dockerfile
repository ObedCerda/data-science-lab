
#Image fo rPython 3.13
FROM python:3.13-slim


#ENV variables 
ENV PYTHONUNBUFFERED = 1  \ 
    PYTHONDONTWRITEBYTECODE =  1 \
    LANG = C.UTF-8 


#System dependencies
RUN apt-get update && apt-get install -y \
    graphviz \
    && rm -rf /var/lib/apt/lists/* 

#Packages 
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


WORKDIR /workspace