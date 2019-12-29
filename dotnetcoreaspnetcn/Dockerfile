FROM mcr.microsoft.com/dotnet/core/aspnet:3.1-buster-slim AS base
COPY fonts /usr/share/fonts/windows/
RUN echo "deb https://mirrors.tuna.tsinghua.edu.cn/debian/ buster main contrib non-free \
    deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ buster main contrib non-free \
    deb https://mirrors.tuna.tsinghua.edu.cn/debian/ buster-updates main contrib non-free \
    deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ buster-updates main contrib non-free \
    deb https://mirrors.tuna.tsinghua.edu.cn/debian/ buster-backports main contrib non-free \
    deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ buster-backports main contrib non-free \
    deb https://mirrors.tuna.tsinghua.edu.cn/debian-security buster/updates main contrib non-free \
    deb-src https://mirrors.tuna.tsinghua.edu.cn/debian-security buster/updates main contrib non-free" > /etc/apt/sources.list
RUN apt-get update && apt-get install fontconfig -y \
    && fc-cache -f -v
CMD ["/bin/bash"]

# ENV ASPNETCORE_VERSION 3.1.0
# 建立aspnet:3.1.0-buster-slim windows中文字体库
#build docker image dotnetcoreaspnetcn:3.1.0-buster-slim