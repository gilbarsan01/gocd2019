
GIT_TAG := $(shell git rev-parse --short HEAD)
USERNAME_DOCKER := gilbarsan
NAME_CONTAINER := curso_gocd_ep6_2019

all:    build tag


#Se genera contenedor con version corta de GIT.
build:
	docker build -t $(NAME_CONTAINER):$(GIT_TAG) .


#Se realiza el tag de la version del contenedor con identificador para realizar el push a Docker HUB.
tag:	
	docker tag $(NAME_CONTAINER) $(USERNAME_DOCKER)/$(NAME_CONTAINER):$(GIT_TAG)
	docker tag $(NAME_CONTAINER) $(USERNAME_DOCKER)/$(NAME_CONTAINER):latest

push:	
	docker push $(USERNAME_DOCKER)/$(NAME_CONTAINER):$(GIT_TAG)	


test:
	@echo $(USERNAME_DOCKER)
	@echo $(NAME_CONTAINER)
