FROM dotnetcoreaspnet-libreoffice:3.0-buster-slim AS base
COPY /src /src
RUN apt-get update && apt-get install imagemagick -y && cp -f /src/policy.xml /etc/ImageMagick-6/policy.xml && rm -rf /src
CMD ["/bin/bash"]