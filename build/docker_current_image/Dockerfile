FROM knowengdev/jupyter_notebooks:06_22_2017
MAINTAINER Dan Lanier <lanier4@illinois.edu>

USER root

RUN rm -rf ${DEV_SRC_LOC}
RUN git clone https://github.com/dlanier/knoweng_transform.git ${DEV_SRC_LOC}

COPY start-notebook.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/start-notebook.sh

USER $NB_USER


# this file         ==>       ~/knoweng_transform/build/docker_current_image/Docker