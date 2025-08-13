# Set An Allow From Subnet in UFW on Linux

To allow traffic from a subnet use this command structure:

```bash
sudo ufw allow from <SUBNET> to any port <PORT> proto <PROTOCOL>
```

Example:

```bash
sudo ufw allow from 10.0.0.0/24 to any port 22 proto tcp
```
