## method 1
`ip addr | grep 'state UP' -A2 | tail -n1 | awk '{print $2}' | cut -f1  -d'/'`

## method 2
`ifconfig | perl -nle 's/dr:(\S+)/print $1/e'`

## method 3
`ifconfig | awk '/inet addr/{print substr($2,6)}'`

## method 4
`ifconfig ens18 | grep 'inet addr:' | cut -d: -f2 | awk '{ print $1}'`
