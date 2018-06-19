### 根据端口号配置不同目录下的资源
	由于资源有限， 想要做的事情比较多， 所以打算配置一下nginx， 
	实现同一个ip不同端口号对应不同的资源， 后续再分配各个端口对应的任务

##### 1 首先是安装nginx， 这个比较简单

```
yum install nginx

```


	默认情况下， nginx配置位置在 /etc/nginx/conf.d/ 目录下， 资源位置在
	/usr/share/nginx/html

##### 2 然后启动nginx

```
service nginx start
```

正常情况下， 会出现 starting   [ok] 的字样， 然后再浏览器访问主机ip即可看到nginx安装成功的提示页

##### 3 我想要做的工作

我想要在/usr/share/nginx/html同级目录下(/usr/share/nginx/*)， 分别创建blog和forum两个资源文件， 然后把主机的81， 82端口分别指向这两个目录下的资源，如果成功的话， 后续就可以分一个目录给gitlab做集成和交付使用。

##### 4 步骤

- 1 需要在 /etc/nginx/conf.d/ 这个目录下创建两个配置文件， 分别为 blog.conf 和 forum.conf

- 2 具体的配置可以借鉴 /etc/nginx/conf.d/default.conf (这个是默认资源的配置文件， 指向/usr/share/nginx/html)

- 3 默认资源的配置文件如下：

```
#
# The default server
#

server {
    listen       80 default_server; # 监听端口
    listen       [::]:80 default_server;
    server_name  _;
    root         /usr/share/nginx/html; # 资源路径
    # root         /usr/share/nginx/blog;

    # Load configuration files for the default server block.
    include /etc/nginx/default.d/*.conf;

    location / {
    }

    error_page 404 /404.html;
        location = /40x.html {
    }

    error_page 500 502 503 504 /50x.html;
        location = /50x.html {
    }

}


```

- 4 根据默认资源配置blog

```
#
# The blog server
#

server
    {
        listen 81; # 监听81端口
        #listen [::]:80;
        server_name [这里填写服务器的ip];
        index index.html index.htm index.php default.html default.htm default.php;
        root  /usr/share/nginx/blog;

        #error_page   404   /404.html;
       

        location ~ .*\.(gif|jpg|jpeg|png|bmp|swf)$
        {
            expires      30d;
        }

        location ~ .*\.(js|css)?$
        {
            expires      12h;
        }

        location ~ /\.
        {
            deny all;
        }

        access_log off;
    }
```

- 5 配置forum

```
#
# The forum server
#

server
    {
        listen 82; # 监听的端口
        #listen [::]:80;
        server_name [这里填写服务器的ip];
        index index.html index.htm index.php default.html default.htm default.php;
        root  /usr/share/nginx/forum;

        #error_page   404   /404.html;

        location ~ .*\.(gif|jpg|jpeg|png|bmp|swf)$
        {
            expires      30d;
        }

        location ~ .*\.(js|css)?$
        {
            expires      12h;
        }

        location ~ /\.
        {
            deny all;
        }

        access_log off;
    }
```

- 6 重启服务

```
service nginx restart
```

- 7 现在就可以通过端口80， 81， 82 分别访问默认的nginx首页， blog页面和forum页面， 如同访问三个不同的站点


