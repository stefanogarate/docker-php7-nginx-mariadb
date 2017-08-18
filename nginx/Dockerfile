FROM nginx

# para test
#RUN apt-get update && apt-get install -y \
#    procps \
#    vim

RUN rm /etc/localtime
RUN ln -s /usr/share/zoneinfo/Chile/Continental /etc/localtime
RUN "date"

RUN mv /etc/nginx/nginx.conf /etc/nginx/nginx.conf.backup
COPY nginx.conf /etc/nginx/nginx.conf
COPY server.conf /etc/nginx/conf.d/server.conf

RUN mv /etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf.backup

RUN echo "upstream php-upstream { server php:9000; }" > /etc/nginx/conf.d/upstream.conf

RUN usermod -u 1000 www-data

CMD ["nginx"]

EXPOSE 443