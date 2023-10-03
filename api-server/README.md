# ThirstMap Backend API Server

## Setup

Make sure you have the tools necessary to run docker, docker compose and Makefiles.

Clone into the project and create a `.env` file and add the following details:

```
POSTGRES_PASSWORD = <password of your choosing>
POSTGRES_USER = postgres
```

Then run the following make commands

```bash
make build
```

```bash
make up
```

```bash
make migrate
```

```bash
make shell
```

Then in the shell that just opened:

```bash
python src/manage.py createsuperuser
```

Further instructions for make commands (such as linting or formatting commands) can be found by running:

```bash
make
```

or

```bash
make help
```