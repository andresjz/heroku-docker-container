FROM nginx:alpine

COPY ./html/ /usr/share/nginx/html/
COPY ./config/ /etc/nginx/

CMD /bin/sh -c 'sed -i "s|PORT|${PORT}|g" /etc/nginx/nginx.conf' && nginx -g 'daemon off;'
