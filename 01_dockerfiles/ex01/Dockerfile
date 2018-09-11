FROM debian

ENV TS3SERVER_LICENSE=accept

RUN apt-get update -y \
&& apt-get install curl -y \
&& apt-get install bzip2 -y \
&& curl -O 'http://dl.4players.de/ts/releases/3.3.1/teamspeak3-server_linux_amd64-3.3.1.tar.bz2' \
&& bzip2 -d teamspeak3-server_linux_amd64-3.3.1.tar.bz2 \ 
&& tar -xf teamspeak3-server_linux_amd64-3.3.1.tar

EXPOSE 9987/udp 10011 30033

WORKDIR /teamspeak3-server_linux_amd64

CMD ["sh", "ts3server_minimal_runscript.sh"]