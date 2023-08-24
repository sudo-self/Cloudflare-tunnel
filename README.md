# CF-tunnel  
## cloudflared tunnel --config /Users/admin/.cloudflared/config.yml run 

<img width="1225" alt="Screenshot 2023-08-24 at 12 27 23 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/3ed98b03-891b-4bcd-8a34-72cc14a8ec39">


### brew install cloudflare/cloudflare/cloudflaredcloudflared
### cloudflared tunnel login 
this creates cert.pem
### cloudflared tunnel create <TUNNEL NAME>
this generates a credentials file
this genertates a subdomain .cfargotunnel.com.
### cloudflared tunnel list
x3 files located here root/.cloudflared

## Config file

### APP
url: http://localhost:8080<br>
tunnel: cloudflared tunnel list (ID GOES HERE)<br>
credentials-file: /root/.cloudflared/197(ID GOES HERE).json

### Network
tunnel: <Tunnel-UUID><br>
credentials-file: /root/.cloudflared/<Tunnel-UUID>.json<br>
warp-routing:<br>
enabled: true

### cat config.yml
confirm config file

### route traffic
cloudflared tunnel route dns <UUID or NAME> <hostname>

### route network 
cloudflared tunnel route ip add <IP/CIDR> <UUID or NAME>

### confirm route
cloudflared tunnel route ip show

### run the tunnel
cloudflared tunnel run <UUID or NAME>

### Pont tunnel to config file 
cloudflared tunnel --config /path/your-config-file.yaml run

### check tunnel status
cloudflared tunnel info <UUID or NAME>
