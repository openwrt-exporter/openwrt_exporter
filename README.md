# openwrt_exporter
OpenWrt/LEDE metrics exporter for Prometheus written in Lua
## Installation
at your openwrt box:

```
# Install luasocket
opkg update
opkg install luasocket

# copy metrics.lua into /bin/
curl -o /bin/metrics.lua https://raw.githubusercontent.com/rbo/openwrt_exporter/master/metrics.lua

# copy initscript into /etc/init.d/
curl -o /etc/init.d/openwrt-exporter https://raw.githubusercontent.com/rbo/openwrt_exporter/master/metrics.initscript

chmod +x /bin/metrics.lua /etc/init.d/openwrt-exporter

# start your exporter and enable on boot
/etc/init.d/openwrt-exporter start
/etc/init.d/openwrt-exporter enable
```

Grafana ScreenShoot
-------------------
![alt text](https://raw.githubusercontent.com/frankiexyz/openwrt_exporter/master/openwrt.png)          
