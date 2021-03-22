FROM python:3.8
ENV PYTHONUNBUFFERED=1
WORKDIR /code
COPY requirements.txt /code/
RUN apt-get update
RUN apt-get install -y libgdal-dev
RUN export CPLUS_INCLUDE_PATH=/usr/include/gdal
RUN export C_INCLUDE_PATH=/usr/include/gdal
RUN pip install GDAL==2.4.0
RUN pip install -r requirements.txt
COPY . /code/

