FROM jupyter/base-notebook
MAINTAINER Dan Lanier <lanier4@illinois.edu>

USER $NB_USER

USER root

# Install packages and their dependencies
RUN apt-get update && apt-get install -y vim python3-pip git libblas-dev liblapack-dev libatlas-base-dev gfortran libfreetype6-dev libxft-dev
RUN conda install numpy==1.11.1 pandas==0.18.1 scipy==0.18.0 scikit-learn==0.17.1 pyyaml

RUN apt-get update && apt-get install python3-dev python3-setuptools

RUN conda install Pillow
RUN conda install IPython
RUN conda install ipywidgets
RUN conda install -c conda-forge jupyter_contrib_nbextensions

USER $NB_USER

# docker build -t knowengdev/jupyter_notebooks:base_image .
# (jupyter/base-notebook in )  https://github.com/jupyter/docker-stacks
# notebook config: init_cell.run_on_kernel_ready
# server config set: notebook.metadata.init_cell.run_on_kernel_ready
#
# this file         ==>       ~/knoweng_transform/build/docker_base_image/Docker
