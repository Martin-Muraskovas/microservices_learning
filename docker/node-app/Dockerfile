# create a script to build an image/microservice of nodejs-app

# containerise the node app



# build the image


# test the image on port 3000 locally


# if works - push it to your dockerhub and share the image

FROM node:latest
RUN apt-get update && apt-get install -y nginx supervisor

COPY nginx.conf /etc/nginx/nginx.conf
WORKDIR /usr/src/app

COPY ./app /usr/src/app

RUN npm install

EXPOSE 80
EXPOSE 3000

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

CMD ["/usr/bin/supervisord"]


