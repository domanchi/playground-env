FROM ubuntu

RUN apt-get update && \
    apt-get install -y netcat && \
    apt-get install -y nginx

## Forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log && \
    ln -sf /dev/stderr /var/log/nginx/error.log

ADD files/ etc/nginx/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
