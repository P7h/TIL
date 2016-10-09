## Turn off firewall on a Linux machine

### CentOS
```bash
sudo service iptables save
sudo service iptables stop
sudo chkconfig iptables off
```

### Ubuntu
```bash
sudo ufw status
sudo ufw off
```
