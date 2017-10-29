FROM python:3.5

RUN pip install dask==0.15.2 distributed==1.18.3 bokeh==0.12.9 jupyter==1.0.0 dask-searchcv==0.1.0
RUN pip install -r https://raw.githubusercontent.com/dnouri/nolearn/master/requirements.txt
RUN pip install git+https://github.com/dnouri/nolearn.git@master#egg=nolearn==0.7.git

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8

WORKDIR /root/
