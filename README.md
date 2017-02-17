## chost(change-host)

Change Host just in command line for MAC. Window doesn't support yet.

## Installation

> npm install -g chost

## Preparation

Edit your host file content like below:

``` 
# work fine(comments)
#==== stable_master
10.165.124.255  www.xx.com
10.165.124.255  www.xx.com.hk
10.165.124.255  globalms.ll.com
10.165.124.255  m.xx.com
10.165.124.255  m.xx.com.hk
#====

# not work(comments)
#==== stable_dev
# 10.165.124.255  www.xx.com
# 10.165.124.255  www.xx.com.hk
# 10.165.124.255  globalms.ll.com
# 10.165.124.255  m.xx.com
# 10.165.124.255  m.xx.com.hk
#====
```

## Example
quick change host:
> chost -n stable_dev

Then host file content turns to:
```
#==== stable_master
# 10.165.124.255  www.xx.com
# 10.165.124.255  www.xx.com.hk
# 10.165.124.255  globalms.ll.com
# 10.165.124.255  m.xx.com
# 10.165.124.255  m.xx.com.hk
#====

#==== stable_dev
10.165.124.255  www.xx.com
10.165.124.255  www.xx.com.hk
10.165.124.255  globalms.ll.com
10.165.124.255  m.xx.com
10.165.124.255  m.xx.com.hk
#====
```

## TODO

- `chost -l` list all available hostname
- `chost -c -e localhost` close all host but localhost
- `chost -c localhost` close certain localhost
- config host helper (auto config your host file)
- make hostFilePath configurable
- unit-test: https://mochajs.org/ like gulp
- support Window