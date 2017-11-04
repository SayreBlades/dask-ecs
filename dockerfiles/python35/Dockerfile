FROM python:3.5

WORKDIR /root/

RUN pip install jupyter==1.0.0
RUN jupyter nbextension enable --py widgetsnbextension
ADD https://github.com/SayreBlades/dask-ecs/tree/master/dockerfiles/python35/*.ipynb .

COPY requirements.txt .
RUN pip install -r requirements.txt

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

