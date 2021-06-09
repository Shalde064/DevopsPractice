FROM jfloff/alpine-python:latest
ADD . /python-flask
WORKDIR /python-flask
RUN pip install flask
EXPOSE 1003
CMD [ "python", "index.py" ]
