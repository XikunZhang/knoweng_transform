FROM knowengdev/jupyter_notebooks:base_notebook
MAINTAINER Dan Lanier <lanier4@illinois.edu>

USER root
ENV BASE_LOC /home/jovyan/pipelines
ENV DEV_SRC_LOC $BASE_LOC/knoweng_transform

RUN rm -rf ${DEV_SRC_LOC}
RUN git clone https://github.com/dlanier/knoweng_transform.git ${DEV_SRC_LOC}

COPY start-notebook.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/start-notebook.sh

USER $NB_USER


# this file         ==>       ~/knoweng_transform/build/docker_current_image/Docker
