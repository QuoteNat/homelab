FROM debian:12

RUN apt-get update && apt-get upgrade -y
RUN	apt-get install -y radicale \
		apache2-utils \
		python3-passlib \
		python3-bcrypt
COPY config.toml /etc/radicale/config
COPY users /users
EXPOSE 5232
CMD ["radicale"]
