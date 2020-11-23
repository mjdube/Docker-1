FROM debian

EXPOSE 9987/udp
EXPOSE 10011 
EXPOSE 30033

RUN apt-get update && apt-get update -y && apt-get install -y wget bzip2 && \
    wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2 && \
    tar -jxvf teamspeak3-server_linux_amd*.tar.bz2 && \
    mv teamspeak3-server_linux_amd64 /usr/local/teamspeak

WORKDIR /usr/local/teamspeak

CMD ["sh", "ts3server_startscript.sh"]