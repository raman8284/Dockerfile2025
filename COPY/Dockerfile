FROM ubuntu
RUN apt install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
COPY qi /usr/share/nginx/html
CMD ["nginx","-g","daemon off;"]