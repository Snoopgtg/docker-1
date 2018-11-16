FROM debian

EXPOSE 30033:30033
EXPOSE 10011:10011
EXPOSE 9987:9987/udp

RUN apt update && apt -y install wget bzip2 \
	&& wget http://dl.4players.de/ts/releases/3.5.0/teamspeak3-server_linux_amd64-3.5.0.tar.bz2 \
	&& tar -xvjf teamspeak3-server_linux_amd64-3.5.0.tar.bz2 \
	&& rm -rf teamspeak3-server_linux_amd64-3.5.0.tar.bz2 \
	&& cd teamspeak3-server_linux_amd64 \
	&& touch .ts3server_license_accepted

WORKDIR teamspeak3-server_linux_amd64
CMD sh ts3server_minimal_runscript.sh

# docker build -t debian-ts3:v1 .
# docker run --name ts3 -p 10011:10011 -p 9987:9987/udp -p 30033:30033 -d debian-ts3:v1