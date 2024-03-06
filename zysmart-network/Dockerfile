FROM alpine:3.13.2 AS zysmart-network-server
RUN mkdir /lib64 && ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2

#定义时区参数
#ENV TZ=Asia/Shanghai
#安装时区数据包
RUN apk add tzdata
#设置时区
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo '$TZ' > /etc/timezone

RUN mkdir -p /usr/local/zysmart-network/
USER nobody:nogroup
