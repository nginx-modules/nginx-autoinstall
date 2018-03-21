# nginx-autoinstall
Automatically compile from source and install Nginx mainline, on Debian 9 (64 bits) and Ubuntu 16.04 LTS .

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=XZNT7SAEYY988) [![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/8bite5d0) 



![screen](https://lut.im/cQ5J1pvOuX/aLcI1sR2LIQKIQxn.png)
## Features
- Latest mainline version, from source
- Optional modules (see below)
- Removed useless modules
- [Custom nginx.conf](https://github.com/Angristan/nginx-autoinstall/blob/master/conf/nginx.conf) (default does not work)
- [Init script for systemd](https://github.com/Angristan/nginx-autoinstall/blob/master/conf/nginx.service) (not provided by default)
- [Logrotate conf](https://github.com/Angristan/nginx-autoinstall/blob/master/conf/nginx-logrotate) (not provided by default)

### Optional modules/features
- [LibreSSL from source](http://www.libressl.org/) (ChaCha20 cipher, HTTP/2 + ALPN, Curve25519, P-521)
- [OpenSSL from source](https://www.openssl.org/) (ChaCha20 cipher, HTTP/2 + ALPN, Curve25519, P-521)
- [ngx_pagespeed](https://github.com/pagespeed/ngx_pagespeed) (Google performance module)
- [ngx_brotli](https://github.com/google/ngx_brotli) (Brotli compression algorithm)
- [ngx_headers_more](https://github.com/openresty/headers-more-nginx-module) (Custom HTTP headers)
- [GeoIP](http://dev.maxmind.com/geoip/geoip2/geolite2/) (GeoIP module and databases)
- [Cloudflare's TLS Dynamic Records Resizing patch](https://github.com/cujanovic/nginx-dynamic-tls-records-patch) (Optmize lantency and throughput for TLS exchanges)
- [VTS](https://github.com/vozlt/nginx-module-vts) (Nginx virtual host traffic status module)

## Install Nginx

Just download and execute the script :
```
wget https://github.com/8bite5d0/nginx-autoinstall/raw/master/nginx-autoinstall.sh
chmod +x nginx-autoinstall.sh
./nginx-autoinstall.sh
```

You can check [configuration examples](https://github.com/8bite5d0/nginx-autoinstall/tree/master/conf) for the custom modules.

## Uninstall Nginx

Just select the option when running the script :

![update](https://lut.im/Hj7wJKWwke/WZqeHT1QwwGfKXFf.png)

You have te choice to delete the logs and the conf.

## Update Nginx

To update Nginx, run the script and install Nginx again. It will overwrite current Nginx files and/or modules.

## Update the script

The update feature downloads the script from this repository, and overwrite the current `nginx-autoinstall.sh` file in the working directory. This allows you to get the latest features, bug fixes, and module versions automatically.

![update](https://lut.im/uQSSVxAz09/zhZRuvJjZp2paLHm.png)

## Logs files
There are two logs files created when running the script.

- `/tmp/nginx-autoinstall-output.log`
- `/tmp/nginx-autoinstall-error.log` (use this one for debugging)

## LICENSE

GPL v3.0
