# Helium-light-gateway-Dragino-setup

Steps to install helium gateway-rs on the gateway
1) ```shell cd /tmp ```
2) ```shell wget -O helium-gateway-v1.0.0-alpha.9-dragino.ipk https://github.com/helium/gateway-rs/releases/download/v1.0.0-alpha.9/helium-gateway-v1.0.0-alpha.9-dragino.ipk ```
3) ```shell opkg install /tmp/helium-gateway-v1.0.0-alpha.9-dragino.ipk ```

Check Gateway Keys- ```shell helium_gateway key info ```
Check Logs- ```shell logread | grep helium_gateway ```
Restart the gateway-rs service- ```shell /etc/init.d/helium_gateway restart ```
