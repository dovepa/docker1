FROM debian

LABEL dpalombo ex01 TeamSpeak docker1

ADD http://dl.4players.de/ts/releases/3.1.1/teamspeak3-server_linux_amd64-3.1.1.tar.bz2 /teamspeak3/

EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011

RUN apt-get update -y \
        && apt-get upgrade -y \
        && adduser --disabled-password --gecos '' ts3 \
        && su ts3 \
        && apt-get install bzip2 \
        && tar -jxvf /teamspeak3/teamspeak3-server_linux_amd64-3.1.1.tar.bz2 \
        && cd teamspeak3-server_linux_amd64 \
        && apt-get install ca-certificates -y \
        && touch .ts3server_license_accepted

ENTRYPOINT ["./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

CMD ["sh"]

#docker run -p 9987:9987/udp -p 10011:10011 -p 30033:30033 test