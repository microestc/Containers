ARG runenv=dotnetcoreaspnetcn
FROM $runenv:3.0.1-buster-slim AS base
COPY /src /src
ENV JAVA_HOME=/usr/java/jre1.8.0_221
ENV PATH=$PATH:/usr/java/jre1.8.0_221/bin
RUN mkdir /usr/java && tar -zxvf /src/jre-8u221-linux-x64.tar.gz -C /usr/java && rm -rf /src
CMD ["/bin/bash"]
# ENV ASPNETCORE_VERSION 3.0.1
#为aspnet:3.0.1-buster-slim建立jre环境
# image: dotnetcoreaspnetcn-jre:3.0.1-buster-slim-8u221