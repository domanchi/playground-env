# Remember that unix versions require sudo for docker commands.

CONTAINER_NAME = nginx-playground
IMAGE_NAME = dev-nginx-pg

default: build
	echo "\033[31mNginx container can be accessed through localhost:2000\033[0m"
	docker run -p 2000:80 --rm --name $(CONTAINER_NAME) -it \
	    $(IMAGE_NAME)

bash:
	docker exec -it $(CONTAINER_NAME) bash

# Every nginx.conf change, we need to reset the server. Rebuilding will do this for us.
build:
	docker build -t $(IMAGE_NAME) .
