ARG runenv=dotnetcoreaspnetcn
FROM $runenv:3.0-buster-slim AS base
COPY /src /src
ENV JAVA_HOME=/usr/java/jre1.8.0_221
ENV PATH=$PATH:/usr/java/jre1.8.0_221/bin
RUN mkdir /usr/java && tar -zxvf /src/jre-8u221-linux-x64.tar.gz -C /usr/java && rm -rf /src
CMD ["/bin/bash"]