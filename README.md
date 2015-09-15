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

```
yum info nginx
...
...
yum install nginx
...
...
```

##### Useage

You can add filePath of site into `nginx.conf`

```
include /etc/nginx/site/*;
```

and then new a file under the `./site`, like: 

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

Of course, also can add into the `nginx.conf` directly

Before use `nginx -s reload` 

You need start nginx firstly with `nginx -p /etc/nginx/nginx.conf`
