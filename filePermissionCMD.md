## chmod recursively 

### Files
`sudo find /var/www -type f -exec chmod 664 {} +`

### Directories
`sudo find /var/www -type d -exec chmod 775 {} +`

### Read default folder Permission
`sudo getfacl /var/www`

### Additional default group's permission 
`sudo setfacl -R -m g:www-data:rwx /var/www`

### follow the parent's groups & permission 
> Set the gid (group id) used for new dirs/files in the /var/www directory - new ones will have group "www-data" just like their parent directory
`sudo chmod -R g+s /var/www`
