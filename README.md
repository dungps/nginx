# nginx config Snippet [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A collection of useful nginx config snippets, all in one place.

## Rewrite and Redirection

### Force www
```
server_name yourdomain.com;
rewrite ^(.*) http://www.yourdomain.com$1 permanent;
```

### Force non-www
```
server_name wwww.yourdomain.com;
rewrite ^(.*) http://yourdomain.com permanent;
```

### Force HTTPS
```
listen 80;

servername yourdomain.com;
rewrite ^(.*) https://yourdomain.com permanent;
```

### Redirect a single page
```
location /page {
  rewrite ^/page(.*) http://$server_name/page2 permanent;
}
```
