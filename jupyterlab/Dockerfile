FROM python:3.9.1-slim-buster

RUN useradd -m -d /home/python python \
    && apt-get upgrade -y \
    && apt-get update \
    && apt-get install -y gcc build-essential libssl-dev libffi-dev python-dev \
    && apt clean  \
    && pip install --upgrade pip \
    && pip install jupyterlab
USER python

WORKDIR /home/python
COPY ./jupyter_lab_config.py .jupyter/.

EXPOSE 8888
 