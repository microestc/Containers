FROM dotnetcoreaspnetcn-jre:3.1.2-buster-slim-8u241 AS base
COPY /src /src
ENV LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib
RUN apt-get update \
    && apt-get install -y \
    build-essential libmagickcore-dev \
    libmagickwand-dev libmagic-dev  \
    libopenjp2-tools libopenjp2-7-dev bc \
    libxinerama1 dbus libsm6 libgio-cil libcairo2 libcups2 \
    && tar xvzf /src/ImageMagick.tar.gz -C /src \
    && cd /src/ImageMagick-7.0.10-0 && ./configure \
    && make && make install \
    && tar -zxvf /src/LibreOffice_6.3.5_Linux_x86-64_deb.tar.gz -C /src \
    && dpkg -i /src/LibreOffice_6.3.5.2_Linux_x86-64_deb/DEBS/*.deb \
    && tar -zxvf /src/LibreOffice_6.3.5_Linux_x86-64_deb_langpack_zh-CN.tar.gz -C /src \
    && dpkg -i /src/LibreOffice_6.3.5.2_Linux_x86-64_deb_langpack_zh-CN/DEBS/*.deb \
    && rm -rf /src && ln -s /usr/local/bin/libreoffice6.3 /usr/local/bin/libreoffice
CMD ["/bin/bash"]
# ENV ASPNETCORE_VERSION 3.1.2
# 安装imagemagick和libreoffice环境
# image: dotnetcoreaspnet-images:3.1.2-buster-slim