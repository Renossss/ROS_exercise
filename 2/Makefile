CUR_DIR = $(shell pwd)

build:
	docker build -t "$$USER-duckiebot-image" --progress=plain .
	docker run --rm -v ./:/workspace --entrypoint=colcon "$$USER-duckiebot-image" build

run:
	docker run --rm -it --network=host --privileged -v /dev/shm:/dev/shm -v ./:/workspace "$$USER-duckiebot-image"

.PHONY: run build