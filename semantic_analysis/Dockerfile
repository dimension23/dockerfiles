FROM jupyter/scipy-notebook

USER root

# python 3 environment is named root
RUN conda install --yes --name root \
  pymongo

# python 3 environment is named python2
RUN conda install --yes --name root \
  pymongo

# install libraries via pip using bash and activating respective environment
RUN ["bash", "-c", "source activate root && pip install twitter"]
RUN ["bash", "-c", "source activate python2 && pip install twitter"]

USER jovyan
