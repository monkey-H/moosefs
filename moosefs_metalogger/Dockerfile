FROM ubuntu:14.04
MAINTAINER hmonkey <5681713@qq.com>

RUN apt-get install -y wget
RUN wget -O - http://ppa.moosefs.com/moosefs.key | apt-key add -
RUN echo "deb http://ppa.moosefs.com/stable/apt/ubuntu/trusty trusty main" > /etc/apt/sources.list.d/moosefs.list
RUN apt-get update && apt-get install -y moosefs-metalogger openssh-server
RUN sed -i "s/MFSMETALOGGER_ENABLE=false/MFSMETALOGGER_ENABLE=true/g" "/etc/default/moosefs-metalogger"

