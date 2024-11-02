SCRIPT_VERSION=v1.0
SCRIPT_AUTHOR=Radu Daia <radu.daia@pm.me>

DOCKER=docker
IMAGE_NAME=yocto_docker_img
IMAGE_VERSION=v1.0.0
CONTAINER_NAME=yocto_docker_container

# TODO: to be edited accordingly for each setup
HOST_MOUNT_PATH=/home/user/yocto-work
CONTAINER_MOUNT_PATH=/home/yocto/work

build:
	$(DOCKER) build -t $(IMAGE_NAME):$(IMAGE_VERSION) .

run: build
	$(DOCKER) run -it --name=$(CONTAINER_NAME) \
		--mount type=bind,source=$(HOST_MOUNT_PATH),target=$(CONTAINER_MOUNT_PATH) \
		$(IMAGE_NAME):$(IMAGE_VERSION) \
		/bin/bash

stop:
	$(DOCKER) stop $(CONTAINER_NAME)

clean: stop
	$(DOCKER) rm -f $(CONTAINER_NAME)