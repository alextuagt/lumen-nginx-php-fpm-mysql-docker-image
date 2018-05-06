FROM nginx

MAINTAINER Jabar Asadi <asadi.jabar@outlook.com>

RUN  nginx -t

# referesh nginx configuration file
COPY nginx.conf /etc/nginx


# define the site as a new host
# make sure file is copied
RUN mkdir /etc/nginx/sites-available/
RUN mkdir /etc/nginx/sites-enabled/

COPY  app.conf /etc/nginx/sites-available/

# create smylink
RUN ln -fs /etc/nginx/sites-available/app.conf /etc/nginx/sites-enabled/app.conf

# remove default site
RUN rm /etc/nginx/sites-enabled/default

RUN echo "upstream php-upstream { server php-fpm:9000; }" > /etc/nginx/conf.d/upstream.conf


RUN usermod -u 1000 www-data

CMD ["nginx"]

EXPOSE 80 443 22 8080
