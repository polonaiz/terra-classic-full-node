FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y tzdata && \
    ln -fs /usr/share/zoneinfo/Asia/Seoul /etc/localtime && \
    dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get update && \
    apt-get install -y vim bash-completion wget sysstat dstat net-tools curl tmux

RUN wget https://github.com/terra-money/classic-core/releases/download/v0.5.22/terra_0.5.22_Linux_x86_64.tar.gz && \
    tar zxvf terra_0.5.22_Linux_x86_64.tar.gz && \
    mv ./terrad /usr/local/bin && \
    which terrad && \
    rm ./terra_0.5.22_Linux_x86_64.tar.gz
