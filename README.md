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

Before use `nginx -s reload` 

You need start nginx firstly with `nginx -p /etc/nginx/nginx.conf`

