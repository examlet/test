build:
	docker build -t fastapi-docker:latest .

start:
	docker run -p 5000:5000 -d --rm --name fastapi-docker fastapi-docker:latest

stop:
	docker stop fastapi-docker