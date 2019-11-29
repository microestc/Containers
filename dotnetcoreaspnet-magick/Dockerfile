FROM dotnetcoreaspnetcn:3.0.1-buster-slim AS base
COPY /src /src
ENV LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib
RUN apt-get update \
    && apt-get install -y \
    build-essential libmagickcore-dev \
    libmagickwand-dev libmagic-dev  \
    libopenjp2-tools libopenjp2-7-dev bc \
    && tar xvzf /src/ImageMagick.tar.gz -C /src \
    && cd /src/ImageMagick-7.0.8-68 \
    && ./configure --with-gslib --with-windows-font-dir=/usr/share/fonts/windows/ \
    && make && make install && make clean && rm -rf /src
CMD ["/bin/bash"]
# ENV ASPNETCORE_VERSION 3.0.1
#为aspnet:3.0.1-buster-slim安装 imagemagick
#image: dotnetcoreaspnet-magick:3.0.1-buster-slim