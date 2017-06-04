Squid
=====

Slim image (13MB) of Squid 3.5.23 running under Alpine Linux 3.6.

How to use
=========

```
docker run -p 3128:3128 jam7/squid3
```

With bespoke configuration:

```
docker run  -v <configPath>/squid.conf:/etc/squid/squid.conf:ro \
            -v <configPath>/cache:/var/cache/squid:rw \
            -v /var/log/squid:/var/log/squid:rw \
            -v /etc/localtime:/etc/localtime:ro \
            -p 3128:3128 \
            jam7/squid3
```

Configuration
=============

Pre-configured like below.

 - Use 4GB diskspace under /var/cache/squid for cache
 - Cache any data upto 32 MB
