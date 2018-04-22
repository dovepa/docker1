FROM ruby:2.5.0

LABEL dpalombo ex02 RoR docker1

RUN apt-get update -y \
        && apt-get upgrade -y \
        && apt-get install nodejs -y \
        && gem install rails \
        && mkdir -p /opt/app

ONBUILD WORKDIR /opt/app
ONBUILD ADD . /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed