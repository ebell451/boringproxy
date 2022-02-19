# FUse boringproxy with home-assistant

## Update compose file

Edit docker-compose.yml and change the following under **commands** for service **boringproxy**
- bp.example.com: your admin domain
- your-user-token: token generated by your server
- your-user-name: the user associated with the server token


## Add tunnel in WebUI

Add new tunnel with the following config

- Domain: domain for this tunnel
- Tunnel Type: **Client TSL**
- Tunnel Port: **Random**
- Client Name: **docker-homeassistant**
- Client Address: **homeassistant**
- Client Port: **8123**

## Start containers
To start the container(s), run the start script in the example folder
```bash
./start.sh
```