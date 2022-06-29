# cznproxy
A public facing proxy for CZNetHub applications.

1. Open ports 80 and 443 on the proxy host's firewall to the subnets making connections.
1. Place in /etc/ssl accessible by root with the proper secure permissions:
   1. a cert in consolidated PEM format named ssl.pem
   1. a corresponding secret key name ssl.key 
1. Customize the URLs and ports in nginx/etc/nginx/conf.d/default.conf for the directives:
   1. `server`
   1. `server_name`
1. `docker-compose up -d`
