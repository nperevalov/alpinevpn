# OpenVPN for Docker on Alpine

Quick instructions: see https://github.com/nperevalov/alpinevpn


Specific for alpine :

```bash
CID=$(docker run -d --privileged -p 1194:1194/udp nperevalov/alpinevpn)
docker run -t -i -p 8080:8080 --volumes-from $CID nperevalov/alpinevpn serveconfig
```
