FROM python:2.7
MAINTAINER Jordi Miguel <jordi.miguel.torrent@gmail.com>

# Tooling to wait for MySQL server to be ready before starting app
COPY wait-for-it.sh /usr/local/bin/
RUN chmod 744 /usr/local/bin/wait-for-it.sh

# Place app in container
COPY app.py requirements.txt /opt/www/
WORKDIR /opt/www
ENV FLASK_APP=app.py

# Install dependencies
RUN pip install -r requirements.txt

EXPOSE 5000
CMD python -m flask run --host=0.0.0.0
