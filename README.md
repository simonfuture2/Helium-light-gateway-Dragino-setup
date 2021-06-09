# Light Hotspot Using Dragino Gateway and Helium Network

Video tutorial : [https://youtu.be/ULMnPckZp1M](https://youtu.be/OuujPVK8f3U)

![alt text](https://github.com/akarsh98/Helium-light-gateway-Dragino-setup/blob/main/Helium/2.JPG)

In this project, we are going to create a Light Hotspot using the Dragino LPS8 Gateway and Helium Network. The Light Hotspot is a Packet forwarder that replicates the action of a real miner but is not capable of mining Helium Tokens based on the Proof of Coverage method. This thing is in beta version now but in the future Helium is planning to incentivize the Hotspots according to the data credits they spend and other factors as well. Nothing is finalized yet and is subject to change but if it is finalized then you might be able to mine Helium tokens by creating your own Packet Forwarder.

![alt text](https://github.com/akarsh98/Helium-light-gateway-Dragino-setup/blob/main/Helium/27.JPG)

We will require a couple of software as well to configure our Gateway as a Light Hotspot. These Softwares are PuTTY, WinSCP, and gateway-rs. We also need to make sure that we are using the latest Dragino firmware and if not we first need to update that. Then we need to configure the Gateway by using some simple steps. One of the most important steps is to install helium gateway-rs on the gateway for which we need to execute the commands given below one by one. 

1)  ``` cd /tmp ``` 
2)  ``` wget -O helium-gateway-v1.0.0-alpha.9-dragino.ipk https://github.com/helium/gateway-rs/releases/download/v1.0.0-alpha.9/helium-gateway-v1.0.0-alpha.9-dragino.ipk ``` 
3)  ``` opkg install /tmp/helium-gateway-v1.0.0-alpha.9-dragino.ipk ``` 

When the above commands are successfully executed we will have the helium gateway-rs installed in our system. After the installation, we are nearly done with the configuration. We only need to do some small changes in a couple of files and we are done. After the configuration, we can check that the Gateway is working fine or not by executing the Check Gateway Keys and Check Logs commands given below which completes the configuration part. 

Check Gateway Keys- ``` helium_gateway key info ``` 

Check Logs- ``` logread | grep helium_gateway ``` 

Restart the gateway-rs service- ``` /etc/init.d/helium_gateway restart  ```

After the completion of the Configuration part, We need to restart our Gateway-rs service using the restart command mentioned above and our Gateway will be ready for testing. What it actually does is that it acts as a channel between the LoRaWAN Node and the Helium Network. So any message that is transferred by the node reaches the Helium Network Console through the Gateway acting as Light Hotspot. We also have with us a pre-configured LoRaWAN Node for testing the hotspot.

![alt text](https://github.com/akarsh98/Helium-light-gateway-Dragino-setup/blob/main/Helium/26.JPG)

To test our Light Hotspot we do not use the Helium Console directly but first, we test the device on Staging Console. There we need to configure the devices with Staging Console and as soon as the LoRaWAN node is powered ON, the messages start transmitting and are visible on the Console as well. By opening the debug Console we can also see the commands running in the background between the node and Gateway. In this way, our Light Hotspot will be ready to be connected to the Helium Network and we can start using it.

![alt text](https://github.com/akarsh98/Helium-light-gateway-Dragino-setup/blob/main/Helium/Capture.JPG)

[PCBONLINE](https://www.pcbonline.com/) is an electronics manufacturing service provider with three production bases. We provide middle and high-end [PCB manufacturing](https://www.pcbonline.com/), PCB assembly, electronic components for assembly, box builds, and PCB design services. Our one-stop services include prototyping and high-volume production. Here are our advantages:

We have been specialized in advanced printed circuit board manufacturing and assembly since 1999. We achieve industry 4.0 manufacturing for aluminum PCBs so that our cost is much lower than other manufacturers. Any levels of manufacturing happen on the same production lines. Our strong manufacturing capability meets any demands of PCB and PCBA orders. All users that register from our website get $100 coupons for online purchases. For bulk orders, we offer discounts, free complete [PCBA samples](https://sys.pcbonline.com/instant-quote/), and free PCBA functional testings. For all PCB and PCBA customers, we offer free design for excellence and one-to-one technical support.
