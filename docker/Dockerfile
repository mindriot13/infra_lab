FROM nginx:alpine
RUN set -xeu ; \ 
apk update && apk add --no-cache shadow ; \
groupmod -g 33 www-data; \
useradd -s /bin/false -M -u 33 -g 33 www-data ; \
sed -i '2s/nginx/www-data/' /etc/nginx/nginx.conf ; \
mv /etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.example
COPY ./nextcloud.conf /etc/nginx/conf.d/



