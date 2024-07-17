image_name = board-game-image
container_name = board-game

build-image:
	docker build -t $(image_name) .

start: delete-container
	docker run -v $(PWD):/app -p 8080:8080 -d --name $(container_name) $(image_name)

stop:
	docker stop $(container_name)

delete-container:
	docker rm $(container_name) -f  || true

delete-image:
	docker image rm $(image_name)

connect_bash:
	docker exec -it $(container_name) sh