# docker build -t docker-debian:sid .
FROM debian:sid

RUN echo "deb http://ftp.us.debian.org/debian/ experimental main non-free contrib" >> /etc/apt/sources.list

RUN apt-get update -qq && \
    apt-get install -qqy -y docker.io=1.13.0~ds1-1

COPY docker-entrypoint.sh /usr/local/bin/

ENTRYPOINT ["docker-entrypoint.sh"]
CMD ["bash"]