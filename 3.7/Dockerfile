ARG PYTHON_VERSION
FROM python:${PYTHON_VERSION}

RUN apt-get update \
    && apt-get install --no-install-recommends -yq \
        git \
    && rm -rf /var/lib/apt/lists/*

ARG POETRY_VERSION
ENV POETRY_VERSION=${POETRY_VERSION}
ENV POETRY_HOME=/opt/poetry

RUN curl -sSL -o /tmp/get-poetry.py https://raw.githubusercontent.com/python-poetry/poetry/${POETRY_VERSION}/get-poetry.py \
    && python /tmp/get-poetry.py \
    && rm /tmp/get-poetry.py

ENV PATH=/opt/poetry/bin:$PATH
