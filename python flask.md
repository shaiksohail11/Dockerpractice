


FROM python:3.10-bullseye
LABEL author="shaik"
LABEL project="python"
RUN git clone https://github.com/Sysnove/flask-hello-world.git && \
cd /flask-hello-world && \
mv hello.py app.py && \
pip3 install flask
EXPOSE 5000
WORKDIR /flask-hello-world
CMD ["flask","run","-h","0.0.0.0"]
