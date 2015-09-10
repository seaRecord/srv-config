# srv-config

## nginx(centos)

##### 采用nginx官方yum源

```
cat /etc/yum.repos.d/nginx.repo

[nginx]
name=nginx repo
baseurl=http://nginx.org/packages/centos/$releasever/$basearch/
gpgcheck=0
enabled=1
```
You can set `nginx.conf` simply like:

```
server {
    listen 80;
    server_name tobegod.com;

    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header host $host;

    location / {
            proxy_pass http://127.0.0.1:10001;
    }
}
```

```
yum info nginx
...
...
yum install nginx
...
...
```

Before use `nginx -s reload` 

You need start nginx firstly with `nginx -p /etc/nginx/nginx.conf`
