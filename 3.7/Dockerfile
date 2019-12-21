ARG PYTHON_VERSION=3.7.6
FROM python:${PYTHON_VERSION}

RUN apt-get update \
    && apt-get install --no-install-recommends -yq \
        git=1:2.20.1-2+deb10u1 \
    && rm -rf /var/lib/apt/lists/*

ARG POETRY_VERSION=1.0.0
ENV POETRY_HOME=/opt/poetry

RUN curl -sSL -o /tmp/get-poetry.py https://raw.githubusercontent.com/python-poetry/poetry/${POETRY_VERSION}/get-poetry.py \
    && python /tmp/get-poetry.py \
    && rm /tmp/get-poetry.py

ENV PATH=/opt/poetry/bin:$PATH
