# CF-tunnel
### brew install cloudflare/cloudflare/cloudflaredcloudflared
### cloudflared tunnel login 
this creates cert.pem
### 
cloudflared tunnel create <NAME>
cloud flared tunnel as a service x 3 files root/.cloudflared

## config.yml
url: http://localhost:8080
tunnel: cloudflared tunnel list (ID GOES HERE)
credentials-file: /root/.cloudflared/197(ID GOES HERE).json

## ID GOES HERE .json
{"AccountTag":"XXX","TunnelSecret":"XXX","TunnelID":"XXX"}

## cert.pem


