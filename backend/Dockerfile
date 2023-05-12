# builds the backend server container, implementing Flask. 

FROM python:3.8-alpine
WORKDIR /app
COPY . .
RUN pip install -r requirments.txt
ENV FLASK_APP=flaskapp.py