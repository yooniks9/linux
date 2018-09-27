### fix webroot permission once and for all

#### change dirs to your web root folder example: 
```
cd /var/www/html
```

#### change permission and ownership
```
sudo find . -type f -exec chmod 664 {} + \
&& sudo find . -type d -exec chmod 775 {} + \
&& sudo chown -R www-data:www-data .
```
