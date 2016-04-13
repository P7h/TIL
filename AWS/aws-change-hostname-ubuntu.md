## Steps to change hostname of a Ubuntu instance on EC2

Connect to Ubuntu EC2 instance in a SSH Client.

### Easiest way in 14.04 and above _only_.
	hostnamectl set-hostname new-hostname

### Check hostname
Run the following command to find the current hostname of the instance:

	hostname

### Fix the new hostname in `hostname` utility
Modify the new hostname thru Use the `hostname` utility.

	sudo hostname new_host_name

### Edit `/etc/hosts`
Add / modify the new hostname in `hosts` file to make the hostname resolvable.

	sudo vi /etc/hosts

Hosts file should be of the following format.

	#IPAddress		Hostname			Alias
	127.0.0.1		localhost			deep.openna.com
	10.23.12.17		new_host_name	 	new_host_name_alias

### Restart your network interface for the changes to take effect
Finally run the following command [or restart the instance] to reflect the changes.

	sudo service hostname restart

OR

	sudo /etc/init.d/networking restart

### Recheck hostname
Run the following command to find the hostname of the instance after the changes:

	hostname
