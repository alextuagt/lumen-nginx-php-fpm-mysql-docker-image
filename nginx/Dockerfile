FROM nginx

MAINTAINER Jabar Asadi <asadi.jabar@outlook.com>

# referesh nginx configuration file 
COPY nginx.conf /etc/nginx

# define the site as a new host
COPY app.conf /etc/nginx/sites-available/

# create smylink
RUN ln -s /etc/nginx/sites-available/app.conf /etc/nginx/sites-enabled/app

# remove default site
RUN rm /etc/nginx/sites-enabled/default

RUN echo "upstream php-upstream { server php-fpm:9000; }" > /etc/nginx/conf.d/upstream.conf

#restart nginx 
RUN service nginx restart

RUN usermod -u 1000 www-data

CMD ["nginx"]

EXPOSE 80 443 22 
