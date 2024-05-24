FROM ubuntu:22.04
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && apt-get install -y wget net-tools vim curl git unzip software-properties-common
ENTRYPOINT tail -f /var/log/mysql/error.log