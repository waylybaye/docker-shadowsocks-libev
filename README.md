# docker-shadowsocks-libev
Shadowsocks libev image with obfs.

https://github.com/shadowsocks/shadowsocks-libev

Latest Version: v3.2.3

Useage:

```yaml
version: '2'
services:
  shadowsocks:
    image: xiocode/shadowsocks-libev
    ports:
      - "10010:8388/tcp"
      - "10010:8388/udp"
    environment:
      - METHOD="chacha20"
      - PASSWORD="1234567890"
      - OBFS_OPTS="obfs=http;obfs-host=www.bing.com"
    restart: always
```
