## Digibeectl Realm Switch

**This script let's you switch between Digibee realms.**

1) Get the script, clonning this repo
```
git clone https://github.com/arturscheiner/dgb-realmswitch.git
```
2) Deploy this script in your $PATH
```
sudo ./dgb-rs -d /usr/local/bin
```
3) Get some HELP
```
dgb-rs -h
```
```
Help Information

Syntax: dgb-rs [-a|l|r|s|u|c|d|h] params

about realm stuff
a	Add a new realm to the switch list
	E.g. -> dgb-rs -a

l	List all the realms configured
	E.g. -> dgb-rs -l

r	Remove a realm from the switch list
	E.g. -> dgb-rs -r realm-name

s	Set an active realm
	E.g. -> dgb-rs -s realm-name

u	Unset the active realm
	E.g. -> dgb-rs -u

about anything else
h	Show this help information
	E.g. -> dgb-rs -h
```

###Obs: These two options just work when running ./dgb-rs inside the repo cloned folder.

```
about this script
c	Check this script deployment
	E.g. -> ./dgb-rs -c

d	Deploy this script into a directory
	E.g. -> sudo ./dgb-rs -d /usr/local/bin
```