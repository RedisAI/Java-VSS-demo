FROM jupyter/minimal-notebook

RUN mkdir /home/jovyan/data

USER root
WORKDIR /home/jovyan
RUN apt-get update && apt-get install -y openjdk-13-jdk
COPY ./java java
COPY ./install.py install.py
RUN python install.py --prefix /opt/conda/ 
RUN rm -rf java install.py
USER $NB_UID
