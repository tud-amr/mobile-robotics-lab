# Lab Router Configuration

<p align="center">
  <img src="amrhub_img.jpg" width="200" />
</p>

The purpose of this router is to simplify the network setup at foreign experiment sites. For example, when you go to the Cyberzoo, you don't want to spend a lot of time to deal with their network setup (which may also change if another group decides to re-configure the router). Therefore, this router has a special DHCP configurations which assigns a dynamic IP to any unkonwn device (e.g. a PhD's laptop) while making sure that the registered robots have a fixed ip. This way, you can just hard-code a robot's IP into your local (ROS) config files.

## Credentials

```
wifi-pass: 40947334
ssid: TP-Link_5F80_5G
router-ip: 192.168.0.1
```

## Static IP Bindings

The following robots have a statically bound IP in the router:

| Robot                                       | Interface     | IP                |
| ------------------------------------------- | ------------- | ----------------- |
| [Jackal 01](../../robots/jackal#Jackal01)   | WIFI          | `192.168.0.101`   |
| [Jackal 02](../../robots/jackal#Jackal02)   | WIFI          | `192.168.0.102`   |
| [Jackal 03](../../robots/jackal#Jackal03)   | WIFI          | `192.168.0.103`   |
| [Jackal 04](../../robots/jackal#Jackal04)   | WIFI          | `192.168.0.104`   |
| [Dingo 1](../../robots/dinova/dingo.md#Dingo1)   | WIFI          | `192.168.0.121`   |
| [Dingo 2](../../robots/dinova/dingo.md#Dingo2)   | WIFI          | `192.168.0.122`   |

# Miscellaneous Technical Notes

- Please don't re-configure this router without coordinating with @lassepe or Thijs Niesten.
- The router software does not resolve hostnames (no local DNS). If you need that feature (e.g. for remote control of the Jackal), edit your `/etc/hosts` file accordingly.
