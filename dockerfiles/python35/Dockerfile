FROM python:3.5

WORKDIR /root/
COPY requirements.txt .
COPY *.ipynb .
RUN pip install -r requirements.txt
RUN jupyter nbextension enable --py widgetsnbextension

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

