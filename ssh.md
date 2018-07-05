##ssh key

### generate ssh key
`ssh-keygen -t rsa -b 4096 -C $EMAILADDRESS`

### copy your public key
`pbcopy < ~/.ssh/id_rsa.pub`

Remote sever ::> paste to remote server ~/.ssh/authorized_keys

## connect to your server
`ssh $USERNAME@$IPADDRESS`