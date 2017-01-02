# Telegram bot Webhook with PHP tutorial #1
preparation:
- OpenSSL (i will use self sign for this tutorial)
- Nginx 
- PHP
- cURL
- Telegram bot with token

Use openssl create private key and public key(PEM file)
```
$ openssl req -newkey rsa:2048 -sha256 -nodes -keyout /etc/nginx/sslkeys/botname.key -x509 -days 365 -out /etc/nginx/sslkeys/botname.pem -subj "/C=CN/ST=Hong Kong/L=Hong Kong/O=Your Company/CN=subdomain.domain.com"
```
config your nginx
```
vim /etc/nginx/conf.d/subdomain.domain.conf
```

```
listen       443 ssl;
server_name  subdomain.domain.com;

root /var/www/bot;
ssl_certificate      /etc/nginx/sslkeys/botname.pem;
ssl_certificate_key  /etc/nginx/sslkeys/botname.key;

ssl_session_cache shared:SSL:50m;
ssl_session_timeout  5m;

#ssl_ciphers  HIGH:!aNULL:!MD5;
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
ssl_ciphers
'ECDHE-RSA-AES128-GCM-SHA256:ECDHE-ECDSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-ECDSA-AES256-GCM-SHA384:DHE-RSA-AES128-GCM-SHA256:DHE-DSS-  
AES128-GCM-SHA256:kEDH+AESGCM:ECDHE-RSA-AES128-SHA256:ECDHE-ECDSA-AES128-SHA256:ECDHE-RSA-AES128-SHA:ECDHE-ECDSA-AES128-SHA:ECDHE-RSA-AES256-SHA384:ECDHE-ECDSA- 
AES256-SHA384:ECDHE-RSA-AES256-SHA:ECDHE-ECDSA-AES256-SHA:DHE-RSA-AES128-SHA256:DHE-RSA-AES128-SHA:DHE-DSS-AES128-SHA256:DHE-RSA-AES256-SHA256:DHE-DSS-AES256-   
SHA:DHE-RSA-AES256-SHA:AES128-GCM-SHA256:AES256-GCM-SHA384:AES128-SHA256:AES256-SHA256:AES128-SHA:AES256-SHA:AES:CAMELLIA:DES-CBC3-SHA:!aNULL:!eNULL:!EXPORT:!   
DES:!RC4:!MD5:!PSK:!aECDH:!EDH-DSS-DES-CBC3-SHA:!EDH-RSA-DES-CBC3-SHA:!KRB5-DES-CBC3-SHA';

ssl_prefer_server_ciphers   on;

location / {
try_files $uri $uri/ /index.php;
index  index.html index.htm index.php;

}
error_page   500 502 503 504  /50x.html;
location = /50x.html {
root   /usr/share/nginx/html;
}

location ~ \.php$ {
try_files $uri =404;
fastcgi_index  index.php;
fastcgi_param  SCRIPT_FILENAME  $document_root$fastcgi_script_name;
include        fastcgi_params;
fastcgi_pass   unix:/var/run/php5-fpm.sock;
}

```
Restart nginx
```
systemctl restart nginx.service
```
Create bot program folder
```
mkdir -d /var/www/bot/[token]/
```
Copy PHP sample code:
https://core.telegram.org/bots/samples/hellobot

```
cd /var/www/bot/[token]/
vim hellobot.php 
```
Change settings:
```
<?php
define('BOT_TOKEN', '12345678:replace-me-with-real-token');
define('API_URL', 'https://api.telegram.org/bot'.BOT_TOKEN.'/');
...

```

Let Telegram knows your webhook, setWebHook:(self sign only, need to upload your public key to telegram)
```
$ curl -F "url=https://subdomain.domain.com/[token]/hellobot.php" -F "certificate=@/etc/nginx/sslkeys/botname.pem" https://api.telegram.org/bot[toke]/setWebhook
```

try start your bot.

DONE
