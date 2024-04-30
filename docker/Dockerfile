FROM jupyter/scipy-notebook as final

USER root
RUN apt-get update && apt-get install -y git
COPY ./requirements.txt ./requirements.txt
RUN mkdir -p /home/jovyan/work
COPY ./.env /home/jovyan/work/.env
ENV GITHUB_ACCESS_TOKEN=
RUN pip3 install --upgrade --force-reinstall -r requirements.txt