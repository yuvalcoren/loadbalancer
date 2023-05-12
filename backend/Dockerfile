# build 3 diffrent flask servers.
# navigate to these servers using nginx loadbalancer
# each server prints the ip in which the server is sitting on

FROM python:3.8-alpine
WORKDIR /app
COPY . .
RUN pip install -r requirments.txt
ENV FLASK_APP=flaskapp.py