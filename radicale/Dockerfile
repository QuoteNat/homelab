FROM debian:12

RUN apt-get update && apt-get upgrade -y 
RUN apt-get install python3-venv -y
RUN python3 -m venv /venv
RUN /venv/bin/pip3 install --upgrade radicale 

EXPOSE 5232
VOLUME /config /data
CMD ["/venv/bin/radicale", "--storage-filesystem-folder=/var/lib/radicale/collections"]
