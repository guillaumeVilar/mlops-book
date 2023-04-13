FROM python:3.11.3-buster

WORKDIR /opt

COPY . .

RUN pip install -r requirements.txt

EXPOSE 8080

CMD gunicorn hello:app -c gunicorn.conf.py