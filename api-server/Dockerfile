FROM python:3.10 AS base

RUN curl -sSL https://install.python-poetry.org | python3 -
ENV PATH="/root/.local/bin:$PATH"
RUN poetry config virtualenvs.create false
COPY . /api-server
WORKDIR /api-server

FROM base AS development

RUN poetry install
CMD ["poetry", "run", "python", "src/manage.py", "runserver", "0.0.0.0:8000"]

FROM base as production

RUN poetry install --without dev
CMD ["poetry", "run", "python", "src/manage.py", "runserver", "0.0.0.0:8000"]
