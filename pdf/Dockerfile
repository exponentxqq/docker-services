FROM centos:7

RUN mkdir -p /usr/share/fonts && \
    yum install fontconfig libX11 libpng15 libXext libXrender libjpeg xorg-x11-fonts-Type1 wget -y && \
    curl http://sjb-files.aizuoye100.com/app/static/pdf-components/PingFang.ttc > /usr/share/fonts/PingFang.ttc && \
    fc-cache && yum install -y openssl  xorg-x11-fonts-75dpi && \
    wget https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6-1/wkhtmltox-0.12.6-1.centos7.x86_64.rpm && \
    rpm -i wkhtmltox-0.12.6-1.centos7.x86_64.rpm && \
    mkdir /var/data

RUN yum install -y libreoffice-core libreoffice-langpack-zh-Hans libreoffice-writer

RUN yum clean all

ARG USER_ID
RUN useradd docker -u ${USER_ID} -g root -m
USER docker
