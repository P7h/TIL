## Steps to change hostname of a CentOS instance on EC2

Connect to CentOS EC2 instance in a SSH Client.

### Check hostname
Run the following command to find the current hostname of the instance:
```
hostname
```

### Edit `/etc/sysconfig/network`
Modify the `HOSTNAME` entry in `/etc/sysconfig/network` to reflect your new hostname.
```
sudo vi /etc/sysconfig/network
```

### Fix the new hostname in `hostname` utility
Modify the new hostname thru Use the `hostname` utility.
```
sudo hostname new_host_name
```

### Edit `/etc/hosts`
Add / modify the new hostname in `hosts` file to make the hostname resolvable.
```
sudo vi /etc/hosts
```

Hosts file should be of the following format.
```
#IPAddress		Hostname			Alias
127.0.0.1		localhost			deep.openna.com
10.23.12.17		new_host_name	 	new_host_name_alias
```

### Restart your network interface for the changes to take effect
Finally run the following command [or restart the instance] to reflect the changes.

```
sudo /etc/rc.d/init.d/network restart
```

### Recheck hostname
Run the following command to find the hostname of the instance after the changes:
```
hostname
```
