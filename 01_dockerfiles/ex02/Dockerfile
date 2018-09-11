FROM ruby

EXPOSE 3000

RUN apt-get update\
	&& apt-get install nodejs -y\
	&& apt-get install build-essential -y\
	&& gem install rails -v 5.0.2

WORKDIR /opt/app

COPY . /opt/app

RUN rails new ex02\
	&& cd ex02 && bundle\
	&& rake db:migrate && rake db:seed