FROM dotnetcoreaspnetcn-jre:3.0-buster-slim-8u221 AS base
COPY /src /src
RUN apt-get update && apt-get install libxinerama1 dbus libsm6 libgio-cil libcairo2 libcups2 -y \
    && tar -zxvf /src/LibreOffice_6.2.7_Linux_x86-64_deb.tar.gz -C /src \
    && dpkg -i /src/LibreOffice_6.2.7.1_Linux_x86-64_deb/DEBS/*.deb \
    && rm -rf /src && ln -s /usr/local/bin/libreoffice6.2 /usr/local/bin/libreoffice
CMD ["/bin/bash"]