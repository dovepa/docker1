FROM ruby

LABEL dpalombo ex02 RoR docker1

RUN apt-get update -y \
        && apt-get upgrade -y 

ENTRYPOINT sh ./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh


#Dockerfile-test
#FROM ft-rails:on-build
#EXPOSE 3000
#CMD ["rails", "s", "-b", "0.0.0.0", "-p" ,"3000"]