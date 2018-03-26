FROM kalilinux/kali-linux-docker

USER root

RUN apt-get update 
RUN apt-get install -y build-essential git net-tools arp-scan nmap rtpflood python python-pip tcpdump
RUN pip install scapy
RUN mv /usr/sbin/tcpdump /usr/local/bin
ENV PATH="/usr/local/bin:${PATH}"

RUN useradd -u 1000 -m rtuser
USER root
WORKDIR /home/root