## Access EC2 Linux instance with SSH Client

To connect to EC2 env in a SSH Client, the following script helps.

    pscp -i some.ppk SSH_Client_Pub.pub root@10.23.12.17:/root/.ssh/
    ssh -i some.pem root@10.23.12.17
    ssh-keygen -f ~/.ssh/SSH_Client_Pub.pub -i >> ~/.ssh/authorized_keys
    
If you have to get / push code or folders from your current EC2 instance to another EC2 instance:

	## Copy a folder from current machine to a remote machine.
    scp -i ~/.ssh/id_rsa -o "UserKnownHostsFile /dev/null" -o StrictHostKeyChecking=no -r SRC_FOLDER root@10.23.12.18:DEST_FOLDER
	
	## Get the source folder from a remote machine to current machine.
	scp -i ~/.ssh/id_rsa -o "UserKnownHostsFile /dev/null" -o StrictHostKeyChecking=no -r root@10.23.12.18:SRC_FOLDER DEST_FOLDER