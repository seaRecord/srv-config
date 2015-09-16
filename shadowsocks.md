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

参数 | 类型 
--- | ---
OS: | [shadowsocks-iOS](https://github.com/shadowsocks/shadowsocks-iOS/releases)
Window: | [shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows/releases)
Browser: | [SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega/releases)
