# Shadowsocks

## Install

Debian / Ubuntu:

```
apt-get install python-pip
pip install shadowsocks
```
CentOS:

```
yum install python-setuptools && easy_install pip
pip install shadowsocks
```

## Server

To run:

```
ssserver -p 443 -k password -m aes-256-cfb
```

To run in the background:

```
sudo ssserver -p 443 -k password -m aes-256-cfb --user nobody -d start
```

To stop:

```
sudo ssserver -d stop
```

To check the log:

```
sudo less /var/log/shadowsocks.log
```

## Client

download the package as you need:

参数 | 地址 | 介绍
--- | --- | ---
OS: | [shadowsocks-iOS](https://github.com/shadowsocks/shadowsocks-iOS/releases) | 无
Window: | [shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows/releases) | 仅监听转发端口，翻墙需配合本地插件(需要确认)

本地插件 | 地址 | 介绍
--- | --- | ---
Browser: | [SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega/releases) | 浏览器插件
Proxifier: | [Proxifier](https://www.proxifier.com/) | 有中文，配置简单
Proxycap: | [Proxycap](http://www.proxycap.com/) | 英文，破解较麻烦，但可实现UDP转发
