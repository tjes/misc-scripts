# GRE service template
Configure and start a GRE tunnel using systemd.

## SETUP
 - Copy the gre@.service template to /etc/systemd/system/
 - Create an instance configuration in /etc with the name `gre-{instance name}`. Define the following values:
   - IFNAME - Name of the GRE Interface
   - IFADDR - IP Address of the GRE Interface
   - LOCALIP - Local IP Address the GRE tunnel will connect with.
   - REMOTEIP - Remote IP Address the GRE tunnel will connect to.
 - Reload systemd: `systemctl daemon-reload`
 - Start the service (see usage)

## USAGE
```
bash$ systemctl enable gre@{instance-name}
bash$ systemctl start gre@{instance-name}
bash$ systemctl reload gre@{instance-name}
bash$ systemctl stop gre@{instance-name}
```

