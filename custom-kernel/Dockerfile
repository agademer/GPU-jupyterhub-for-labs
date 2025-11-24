#FROM quay.io/jupyter/base-notebook:latest
FROM quay.io/jupyter/pytorch-notebook:cuda12-notebook-7.5.0

USER root
RUN apt update && apt install tree nvtop && apt clean

USER jovyan

COPY ./WARNING.txt /home/jovyan/work/

COPY ./requirements.txt /build/requirements.txt

RUN pip install -r /build/requirements.txt
