ARG runenv=dotnetcoreaspnetcn
FROM $runenv:3.1.2-buster-slim AS base
COPY /src /src
ENV JAVA_HOME=/usr/java/jre1.8.0_241
ENV PATH=$PATH:/usr/java/jre1.8.0_241/bin
RUN mkdir /usr/java && tar -zxvf /src/jre-8u241-linux-x64.tar.gz -C /usr/java && rm -rf /src
CMD ["/bin/bash"]
# ENV ASPNETCORE_VERSION 3.1.2
#为aspnet:3.1.2-buster-slim建立jre环境
# image: dotnetcoreaspnetcn-jre:3.1.2-buster-slim-8u241