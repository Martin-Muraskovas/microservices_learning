# this dockerfile is to build an image/microservice to host static webpage


# find a suitable base image to use (nginx image is good)

FROM nginx:latest

# who is building it
LABEL MAINTAINER=MARTINMURASK123@GMAIL.COM

# copy the index.html from localhost to /usr/share/nginx/html/
COPY index.html /usr/share/nginx/html/

# which ports to expose/enable
EXPOSE 80

# launch the server / nginx official command using CMD
CMD ["nginx", "-g", "daemon off;"]

# ensure to create this Dockerfile where the index.html file is located

