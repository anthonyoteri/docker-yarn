FROM alpine:latest
MAINTAINER Anthony Oteri <anthony.oteri@gmail.com>

RUN apk update \
    && apk add \
        nodejs \
	curl \
	bash \
	gnupg

RUN touch $HOME/.profile \
    && curl -L -o - https://yarnpkg.com/install.sh | bash \
    && mkdir -p /app
     
WORKDIR "/app"
VOLUME ["/app"]

ENV PATH=$PATH:/root/.yarn/bin/
CMD [ "/root/.yarn/bin/yarn" ]
