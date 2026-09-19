FROM nginx:alpine@sha256:62ff2089abf5a9ed33bd232895bef5e22f7bb4b200675cec49a5ebc48e3d4ac8
RUN apk add gettext
COPY ./nginx.conf /etc/nginx/nginx.conf
CMD envsubst '\$DOMAIN' < /etc/nginx/nginx.conf > /etc/nginx/nginx.conf && nginx -g 'daemon off;'
