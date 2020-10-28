FROM ubuntu

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y pandoc && \
    apt-get install -y texlive texlive-xetex latex-cjk-all texmaker

RUN apt-get install -y xfonts-75dpi xfonts-base

COPY ./wkhtmltox_0.12.6-1.focal_amd64.deb /opt

COPY ./NotoSansCJK-Regular.ttc /usr/share/fonts/custom/

RUN mkfontscale && mkfontdir && fc-cache -fv