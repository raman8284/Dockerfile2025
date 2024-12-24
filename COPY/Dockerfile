
FROM ubuntu:24.04

RUN apt-get update && apt-get install -y \
    nginx \
    && rm -rf /var/lib/apt/lists/*

COPY nginx.conf /etc/nginx/nginx.conf
COPY qi/ /usr/share/nginx/html/
CMD ["nginx", "-g", "daemon off;"]



