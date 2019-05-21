
GIT_TAG := $(shell git rev-parse --short HEAD)
USERNAME_DOCKER := gilbarsan
NAME_CONTAINER := curso_gocd_ep6_2019

all:    build tag


build_and_tag:  build tag

build:
	docker build -t $(NAME_CONTAINER):$(GIT_TAG) .


tag:	
	docker tag $(NAME_CONTAINER) $(USERNAME_DOCKER)/$(NAME_CONTAINER):$(GIT_TAG)
	docker push $(USERNAME_DOCKER)/$(NAME_CONTAINER):$(GIT_TAG)	


test:
	@echo $(USERNAME_DOCKER)
	@echo $(NAME_CONTAINER)
