# Software Debugging

Often the first symptoms of an issue with the kit manifest as a software error, regardless of whether the underlying issue is actually a software or a hardware issue. This page documents some methods which can be used with the kit to dig deeper into software issues.

The first port of call with software issues should be the status LEDs on the Brain Board, as well as any information in the logs, either in the `log.txt` file or via the WiFi interface.

## Getting a Command Prompt

Accessing a command prompt on the robot is the first step to digging deeper into many issues on the robot.

1. Connect to the Robot via WiFi or ethernet.
1. You can then SSH to the robot using a terminal (Linux / MacOS) or PuTTY: `ssh root@robot.lan`.

If the DNS isn't working, you can use the IP address of the robot: `ssh root@192.168.32.1`.

There are two command line file editors available: `nano` and `vim`.

USB drives are mounted at `/var/run/media/astoria/`

## Logging

- `dmesg -w` - View and follow the kernel log
- `udevadm monitor` - Monitor udev events
- `journalctl -f` - View and follow journal logs
- `journalctl -fu astdiskd` - View and follow astdiskd logs
- `journalctl -fu astprocd` - View and follow astprocd logs
- `journalctl -fu astmetad` - View and follow astmetad logs
- `journalctl -fu astwifid` - View and follow astwifid and hostapd logs
- `journalctl -fu kchd` - View and follow astwifid and hostapd logs
- `journalctl -fu servohack` - View and follow astwifid and hostapd logs
- `cat /var/lib/misc/dnsmasq.leases` - List DHCP leases on robot WiFi
- `mosquitto_sub -v -t "astoria/#"` - Monitor MQTT Event Bus messages

### Astoria Specific Commands

- `astctl usercode show` - Show information about usercode
- `astctl usercode log` - Follow the usercode logs
- `astctl usercode trigger` - Trigger the virtual start button
- `astctl usercode kill` - Kill any running usercode
- `astctl usercode restart` - Restart any running usercode
- `astctl list-disks` - List inserted USB drives and their types
- `astctl metadata show` - Show all current metadata
- `astctl metadata set <key> <val>` - Set a metadata attribute
- `cat /var/srobo/cache/astmetad-metadata.json` - View the metadata cache

### Misc

- `nft -f /etc/nftables` - Reload firewall
- `nano /etc/nftables` - Edit the firewall configuration
