FROM alpine:3.9

ARG APK_MIRROR=mirrors.aliyun.com

RUN sed -i "s/dl-cdn.alpinelinux.org/${APK_MIRROR}/g" /etc/apk/repositories

RUN apk add --no-cache bash nfs-utils

EXPOSE 2049

ENTRYPOINT ["/start-container.sh"]

COPY configure-exports.sh / \
     start-container.sh /
