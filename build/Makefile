CUR_DATE=`date +'%m_%d_%Y'`
LATEST_IMAGE = 'latest'

# lanier4@illinois.edu      -- build jupyter notebooks images for KnowEnG


build_latest:
	cd docker_current_image/; docker build --no-cache -t knowengdev/jupyter_notebooks:$(LATEST_IMAGE) .
# 4 minutes

push_latest:
    docker push knowengdev/jupyter_notebooks:$(LATEST_IMAGE)



build_base_image:
	cd docker_base_image/; docker build --no-cache -t knowengdev/jupyter_notebooks:base_notebook .
# 18 minutes

push_base_image:
	docker push knowengdev/jupyter_notebooks:base_image



login_to_dockerhub:
	docker login --username=$(username) --email=$(email)

# docker run -v `pwd`:/home/jovyan/work -it --rm -p 8888:8888 knowengdev/jupyter_notebooks:latest
