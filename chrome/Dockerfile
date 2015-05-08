FROM fedora:21
MAINTAINER "Ye Myat Kaung (Maverick)" <mavjs@mavjs.org>

RUN yum install https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm -y && \
    yum install https://dl.google.com/linux/direct/google-talkplugin_current_x86_64.rpm -y

ENTRYPOINT [ "/usr/bin/google-chrome" ]
CMD [ "--user-data-dir=/data", "--force-device-scale-factor=1.5"]
