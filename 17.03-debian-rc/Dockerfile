# docker build -t docker-debian:sid .
FROM debian:sid

RUN apt-get update -qq && \
    apt-get install -qqy -y docker.io

COPY docker-entrypoint.sh /usr/local/bin/

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["bash"]