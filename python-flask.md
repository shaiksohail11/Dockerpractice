FROM python:bullseye
RUN git clone https://github.com/Sysnove/flask-hello-world.git && cd /flask-hello-world && mv hello.py app.py 
RUN pip3 install flask
CMD ["flask", "run", "-h", "0.0.0.0"]