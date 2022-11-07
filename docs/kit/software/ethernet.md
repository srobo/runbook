# Ethernet

The Brain Board has an Ethernet port which can be used in addition or as an alternative to WiFi.

It will provide access to the WiFi interface and SSH.

## Ethernet and WiFi

The Ethernet port will attempt to get an IPv4 address using DHCP from any network that it is connected to. This works well with home routers and some school networks, although most are too locked down to allow this.

The WiFi Interface and SSH can be accessed from the upstream network using the IP address that is allocated, you will need to check the DHCP leases on the network's router. The DNS for `robot.lan` will probably not work.

Any devices connected to the WiFi will be able to access the upstream network and Internet if available. This is useful for debugging as you can access both the Internet and the WiFi interface at the same time.

## Standalone Ethernet

It is also possible to connect a laptop directly to the Brain Board using Ethernet. This tends to work best using Linux, but is also possible using MacOS and Windows.

The key issue here is that no IP address will be assigned to your laptop by the Brain Board. There are two approaches that we can use to work around this.

### Using Link-local Addressing

By default, IPv6 link-local addresses will be available on both the Brain Board and your laptop. Some operating systems may decide to disconnect as there is a lack of connection. You may be able to configure it to ignore the lack of Internet.

You can discover the link local address of the Brain Board using the following commands:

```bash
interface=enp0s25  # The interface for your Ethernet port
addr=$(ping -6nLc 1 ff02::1%$interface | grep "icmp_seq" | sed -r "s/64 bytes from //;s/: icmp_seq=(.)+"//)
ssh root@$addr
```

### Using your Laptop as a DHCP server

MacOS and Linux will allow your to configure your laptop as a DHCP server, which will then allocate an address to the brain board.

#### NetworkManager (Most Linux Desktops)

- On Ubuntu open Network connections from the applet or via command line `nm-connection-editor`.
- Click add a connection.
- Select type `ethernet`.
- Choose an appropriate name, e.g `robot-ethernet` and select create.
- Navigate to the IPv4 Settings tab.
- Select Method `Shared to other computers`.
- Start the connection from the UI, or by running `nmcli connection up robot-ethernet`

#### MacOS

- Open System Preferences.
- Open the Sharing preference pane and select Internet Sharing in the left-hand Service list.
- From the “Share your connection from” menu, select Wi-Fi.
- From the “To computers using” list, check the box next to your ethernet adapter. (You may see more than one listed depending on the interfaces on your computer.)
- Check the Internet Sharing box to start sharing.
- Ignore the warning. Click Start.