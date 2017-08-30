FROM docker:17.06.0-ce-git
MAINTAINER Dragos Bulugean

RUN apk --no-cache update && \
    apk add ca-certificates wget && \
    update-ca-certificates && \
    apk --no-cache add python py-pip py-setuptools ca-certificates groff less && \
    pip --no-cache-dir install awscli && \
    rm -rf /var/cache/apk/*