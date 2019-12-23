Simple WireGuard vpn manager


This is more PoC than full tool. Public domain.


This script allow to setup simple [WireGuard](https://www.wireguard.com/) server and manage client configuration.

This is only proof on concept (it's not too safe solution - key are generated on the server, etc, etc...). 
Example usage:
```
# Setup server
# Create server ip pool (for VPN network)
# First IP from the pool will be used as server internal address
./wg_simple ip set 172.8.0.0/16

# Where IP is server public IP address
./wg_simple setup <IP>

# Add new client/user
./wg_simple add user1

# Show current server configuration
wg show

# Generarte user configuration (should be copied to the client device)
./wg_simple show user1
```

Other opitions
```
# IP addresses are auto allocated from definied pool

# Delete user 
./wg_simple del user1

# After delete IP will not be reclimed
```
