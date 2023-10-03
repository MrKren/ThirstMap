.PHONY: help # Generate list of targets with descriptions
help:
	@grep '^.PHONY: .* #' Makefile | sed 's/\.PHONY: \(.*\) # \(.*\)/\1	\2/' | expand -t20

.PHONY: fmt # Formats .py files using isort and black
fmt:
	cd src/ && poetry run isort . && poetry run black .

.PHONY: lint # Lints .py files using isort and flake8
lint:
	cd src/ && poetry run flake8 && poetry run isort . -c

.PHONY: build # Builds the docker image used for development
build:
	docker compose build

.PHONY: up # Starts the development environment of the app
up:
	docker compose up

.PHONY: shell # Shells into the docker compose django container
shell:
	docker compose exec -it django /bin/bash

.PHONY: makemigrations # Creates Django migrations
makemigrations:
	docker compose exec django python src/manage.py makemigrations

.PHONY: migrate # Runs Django migrations
migrate:
	docker compose exec django python src/manage.py migrate

.PHONY: django-shell # Runs Django shell (requires django container to be running)
django-shell:
	docker compose exec django python src/manage.py shell
