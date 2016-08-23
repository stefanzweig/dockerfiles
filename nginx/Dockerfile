FROM gliderlabs/alpine:latest
MAINTAINER Stefan Zweig <stefan.zweig@gmail.com>

RUN apk add --update \
	nginx \
	&& rm -rf /var/cache/apk/*

RUN ln -sf /dev/stdout /var/log/nginx/access.log && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80 443

CMD ["nginx", "-g", "daemon off;"]