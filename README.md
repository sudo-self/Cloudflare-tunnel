# CF-tunnel  
## cloudflared tunnel --config /Users/admin/.cloudflared/config.yml run 

<img width="1225" alt="Screenshot 2023-08-24 at 12 27 23 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/3ed98b03-891b-4bcd-8a34-72cc14a8ec39">


<img width="1139" alt="Screenshot 2023-08-24 at 12 44 16 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/8c29e469-2ab4-4eb3-b0f6-9c117092dda2">


### brew install cloudflare/cloudflare/cloudflaredcloudflared
### cloudflared tunnel login 
this creates cert.pem
### cloudflared tunnel create <TUNNEL NAME>
this generates a credentials file
this genertates a subdomain .cfargotunnel.com.
### cloudflared tunnel list
### x3 files located here root/.cloudflared
<img width="632" alt="Screenshot 2023-08-24 at 12 32 40 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/f1e92ab4-6523-4c7d-bf24-e6ce5f6c7d4e">
### APP
url: http://localhost:8080<br>
tunnel: cloudflared tunnel list (ID GOES HERE)<br>
credentials-file: /root/.cloudflared/197(ID GOES HERE).json
### Network
tunnel: <Tunnel-UUID><br>
credentials-file: /root/.cloudflared/<Tunnel-UUID>.json<br>
warp-routing:<br>
enabled: true
### route traffic
cloudflared tunnel route dns <UUID or NAME> <hostname>
<img width="1053" alt="Screenshot 2023-08-24 at 12 39 14 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/b815c9a4-ba58-4645-9b05-879f3aad0eb8">
### confirm route
cloudflared tunnel route ip show
### run the tunnel
cloudflared tunnel run <UUID or NAME>
### Pont tunnel to config file 
cloudflared tunnel --config /path/your-config-file.yaml run
### check tunnel status
cloudflared tunnel info <UUID or NAME>
<img width="1139" alt="Screenshot 2023-08-24 at 12 44 16 AM" src="https://github.com/sudo-self/CF-tunnel/assets/119916323/287c65cf-87c1-4b9a-b2e7-9a91143d5497">



