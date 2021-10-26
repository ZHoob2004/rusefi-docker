FROM nginx
ADD https://download.phpbb.com/pub/release/3.2/3.2.11/phpBB-3.2.11.zip /build/phpBB-3.2.11.zip
WORKDIR /var/www/phpBB3
RUN apt-get update && apt-get install unzip -y
RUN unzip /build/phpBB-3.2.11.zip

FROM nginx
COPY --from=0 /var/www/phpBB3/* /var/www/forum
COPY default.conf /etc/nginx/conf.d/default.conf