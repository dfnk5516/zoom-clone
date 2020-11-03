# nginx기반
FROM nginx

# nginx.conf파일을 해당 파일에 붙여넣는다
COPY default.conf /etc/nginx/conf.d/default.conf
USER root
RUN apt update && apt install -y certbot && apt install -y python-certbot-nginx
EXPOSE 3032