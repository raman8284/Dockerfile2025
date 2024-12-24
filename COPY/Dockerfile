FROM ubuntu:latest
RUN apt install nginx -y
#RUN rm -rf /var/lib/apt/lists/*
RUN rm -rf /usr/share/nginx/html/index.html
COPY qi/ /var/www/html/
CMD ["nginx", "-g", "daemon off;"]