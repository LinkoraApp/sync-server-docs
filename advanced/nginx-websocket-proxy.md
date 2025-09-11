# Nginx WebSocket Proxy Configuration

As you can see in the legendary lengthy conversation we had in [this issue](https://github.com/LinkoraApp/sync-server/issues/5):

## Problem
WebSocket connections fail with error: `Handshake exception, expected status code 101 but was 400`

## Solution
Add WebSocket headers to Nginx config:

```nginx
location / {
    proxy_pass http://localhost:45454;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
}
```

## Why It's Needed
WebSocket connections require HTTP upgrade headers to switch from HTTP to WebSocket protocol. Without these headers, the handshake fails and real-time sync doesn't work.

## Your script should look similar to this:
```nginx
server {
    listen 443 ssl default_server;
    listen [::]:443 ssl default_server;
    listen 80;
    server_name your-domain.com;
    
    ssl_certificate /etc/ssl/certs/nginx-selfsigned.crt;
    ssl_certificate_key /etc/ssl/private/nginx-selfsigned.key;
    
    location / {
        proxy_pass http://localhost:45454;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection "upgrade";
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```
