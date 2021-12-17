FROM ubuntu:focal

RUN apt-get update && apt-get -y upgrade \
    && echo "8 48" | apt-get install -y software-properties-common wget curl \
    && add-apt-repository universe \
    && wget https://packages.ntop.org/apt-stable/20.04/all/apt-ntop-stable.deb \
    && apt install -y ./apt-ntop-stable.deb \
    && apt-get install -y ntopng \
    && systemctl enable ntopng

RUN mkdir /ntopngcustom \
    && chmod 777 /ntopngcustom