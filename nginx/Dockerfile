FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*

COPY . /usr/share/nginx/html

RUN rm /etc/nginx/nginx.conf

COPY ./.nginx/nginx.conf /etc/nginx

RUN rm -rf /etc/nginx/conf.d/*

COPY ./.nginx/default.conf /etc/nginx/conf.d

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
