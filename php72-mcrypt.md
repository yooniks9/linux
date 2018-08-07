## install dependency
`sudo apt-get -y install gcc make autoconf libc-dev pkg-config ibmcrypt-dev php-pear`
## install mcrypt
`sudo pecl install --nodeps mcrypt-snapshot`
## add to php module
`echo "extension=mcrypt.so" | sudo tee -a /etc/php/7.2/apache2/conf.d/20-mcrypt.ini`
