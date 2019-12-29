FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
ADD ffmpeg-git-amd64-static.tar.xz /
RUN mv /ffmpeg*/ffmpeg /usr/bin/ && rm -rf /ffmpeg*
CMD [ "/bin/bash" ]
# ENV ASPNETCORE_VERSION 3.1.0
# aspnet:3.1.0-buster-slim 安装ffmpeg环境
# image: dotnetcoreaspnet-ffmpeg:3.1.0-buster-slim