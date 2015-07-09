FROM fedora:latest
MAINTAINER "Ye Myat Kaung (Maverick)" <mavjs@mavjs.org>

RUN dnf install https://dl.google.com/linux/direct/google-chrome-stable_current_x86_64.rpm -y && \
    dnf install https://dl.google.com/linux/direct/google-talkplugin_current_x86_64.rpm -y && \
    dnf install https://fpdownload.macromedia.com/get/flashplayer/pdc/11.2.202.460/flash-plugin-11.2.202.460-release.x86_64.rpm -y && \
    dnf clean all
ENTRYPOINT [ "/usr/bin/google-chrome" ]
CMD [ "--user-data-dir=/data" ]
