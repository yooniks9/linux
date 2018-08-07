## rsync recursively only update

> rsync -avz $SOURCE $DESTINAION

`rsync -avz $SOURCE/. $USERNAME@$IPADDRESS:$DESTINAION/.`

## rsync with pem key authenication, Copy your id_rsa.pub into /home/$USER/.ssh/authorized_keys

`rsync -rave "ssh -o StrictHostKeyChecking=no -o UserKnownHostsFile=/dev/null -i /home/$USER/KEY.pem" root@$IPADDRESS:$SOURCE/ $DESTINAION/`
