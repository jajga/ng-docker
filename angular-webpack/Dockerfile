FROM nginx
MAINTAINER Narendra
RUN apt-get update && apt-get install -my wget gnupg
RUN apt-get update && apt-get install -y \
	curl 
RUN curl -sL https://deb.nodesource.com/setup_7.x | bash -
RUN apt-get update && apt-get install -y \
	nodejs
RUN node -v	
RUN apt-get install -y npm
RUN npm -v
#COPY nginx/localhost.crt /etc/ssl/certs/localhost.crt
#COPY nginx/localhost.key /etc/ssl/private/localhost.key
#RUN ls /etc/ssl/certs  
#RUN cp -a /angular/dist/. /usr/share/nginx/html/
#COPY nginx/default.conf /etc/nginx/conf.d/default.conf
RUN mkdir /usr/src/app 
WORKDIR /usr/src/app
COPY . .
EXPOSE 80 82 443 4200 8080

