### Install nginx with proxy_pass or fastcgi + php-fpm (5.4,5.6,7.2) on CentOS 7

In file nginx var can choose install option
Option source
```YAML
---
#Local arhive
index_zip: index.zip
#OR git repo
repo_git: https://github.com/DenisKupreev/testpagephp.git
```
Virtual host option
```YAML
domain: site.com
server_listen: "10.0.10.2"
server_name: "site.com www.site.com"
index: "index.php"
```
Option backend
```YAML
####Use proxy_pass
 proxy_pass: "10.0.10.2"
 proxy_pass_port: "8080"
 proxy_pass_cache: "on"
#OR
####Use fast_cgi + PHPFPM 5.4 5.6 7.2
phpfpm: "on"
version_php: "5.6"
fastcgi_pass: "127.0.0.1"
fastcgi_pass_port: "9000"
fastcgi_pass_cache: "on"
```
Option SSL
```YAML
####Use SSL
use_ssl: "on"
port_ssl: "443"
ssl_pem: "site.com.pem"
ssl_key: "site.com.kay"

```
To disable option, comment on them
