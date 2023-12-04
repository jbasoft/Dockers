# install  Fireawall

**Step 1 – Installing UFW**

Debian does not install UFW by default. If you followed the entire Initial Server Setup tutorial, you will have installed and enabled UFW. If not, install it now using apt:
```
sudo apt install ufw
```

**Step 2 — Allowing SSH Connections**

```
sudo ufw allow ssh
```
However, you can actually write the equivalent rule by specifying the port instead of the service name. For example, this command produces the same result as the one above:
```
sudo ufw allow 22
```

**Step 3 — Allowing Other Connections**

You can do this for HTTP on port 80, which is what unencrypted web servers use. To allow this type of traffic, you would type:
```
sudo ufw allow http
```
You can also do this for HTTPS on port 443, which is what encrypted web servers use. To allow this type of traffic, you would type:
```
sudo ufw allow https
```
In both scenarios, specifying the ports would also work, with HTTP being 80 and HTTPS being 443. For example:
```
sudo ufw allow 80
```

**Specific Port Ranges**

You can specify port ranges with UFW. For example, some applications use multiple ports instead of a single port.

For example, to allow X11 connections, which use ports 6000-6007, use these commands:
```
sudo ufw allow 6000:6007/tcp
sudo ufw allow 6000:6007/udp
```

**Specific IP Addresses*

When working with UFW, you can also specify IP addresses. For example, if you want to allow connections from a specific IP address, such as a work or home IP address of 203.0.113.4, you need to specify from and then the IP address:
```
sudo ufw allow from 203.0.113.4
```

**Step 4 — Enabling UFW**

To enable UFW, use this command:
```
sudo ufw enable
```
The firewall is now active. To see the rules that you have set, run this command:
```
sudo ufw status verbose
```

By Rule Number

The UFW status command has the numbered option, which displays numbers next to each rule:
```
sudo ufw status numbered
```

**Step 5 — Deleting Rules**

If you’re using the rule number to delete firewall rules, the first thing you’ll want to do is get a list of your firewall rules.

```
sudo ufw status numbered
```
```
sudo ufw delete 1
```

**Step 6 — Disabling or Resetting UFW**

If you decide you don’t want to use UFW, you can disable it with this command:
```
sudo ufw disable
```
Any rules that you created with UFW will no longer be active. You can always run sudo ufw enable if you need to activate it later.

If you already have UFW rules configured, but you decide that you want to start over, you can use the reset command:
```
sudo ufw reset
```


