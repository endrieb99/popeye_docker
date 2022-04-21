FROM python:latest

MAINTAINER Endri Bida

WORKDIR /code

COPY . /code

RUN pip3 install -r requirements.txt

EXPOSE 80

CMD ["python", "app.py"]