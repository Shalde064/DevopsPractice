FROM python
ADD . /python-flask
WORKDIR /python-flask
RUN pip install flask flask_cors
EXPOSE 1003
CMD [ "python", "index.py" ]
