FROM alpine:latest

ARG version=fv1.0.0

# version
ENV VERSION ${version}

WORKDIR /app

RUN apk add --no-cache --virtual .bootstrap-deps wget ca-certificates \
    && wget https://github.com/foxiswho/docker-govanityurls/releases/download/${VERSION}/govanityurls-linux-amd64 -o govanityurls \
    && chmod +x  govanityurls \
    && ln -s /app/govanityurls /usr/bin/govanityurls \
    && apk del .bootstrap-deps

EXPOSE 8080

CMD /app/govanityurls
