FROM ubuntu:18.04
MAINTAINER abhishekhdpatil6899@gmail.com

RUN apt-get update -y
RUN apt-get install python3-pip -y
RUN apt-get install gunicorn3 -y

COPY requirment.txt requirment.txt
COPY todo_flask /opt/

RUN pip3 install -r requirment.txt
WORKDIR /opt/

CMD ["gunicorn3", "-b", "0.0.0.0:8034", "app:app", "--workers=5"]
