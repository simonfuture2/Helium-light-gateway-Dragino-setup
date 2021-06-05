# Helium-light-gateway-Dragino-setup

Steps to install helium gateway-rs on the gateway
1) ``` cd /tmp ```
2) ``` wget -O helium-gateway-v1.0.0-alpha.9-dragino.ipk https://github.com/helium/gateway-rs/releases/download/v1.0.0-alpha.9/helium-gateway-v1.0.0-alpha.9-dragino.ipk ```
3) ``` opkg install /tmp/helium-gateway-v1.0.0-alpha.9-dragino.ipk ```

Check Gateway Keys- ``` helium_gateway key info ```

Check Logs- ``` logread | grep helium_gateway ```

Restart the gateway-rs service- ``` /etc/init.d/helium_gateway restart ```
