# cznproxy
A public facing proxy for CZNetHub applications.

1. Open ports 80 and 443 on the proxy host's firewall to the subnets making connections.
1. Place in the proxy host's `/opt/certs` (owned `root:root` and mode `555`):
   1. a cert in consolidated PEM format named `ssl.pem` (owned `root:root` and mode `444`)
   1. a corresponding secret key named `ssl.key` (owned `root:root` and mode `400`)
1. Customize the URLs and ports in `./nginx/etc/nginx/conf.d/default.conf` for the directives:
   1. `upstream`
   1. `server`
   1. `server_name`
1. `docker-compose up -d`
