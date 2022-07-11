## Digibeectl Realm Switch

**This script let's you switch between Digibee realms.**
**Before using it, make sure you have digibeectl installed on your computer**



1) Install digibeectl on your MAC or LINUX computer as described on [Digibeectl Official Documentation](https://intercom.help/godigibee/en/articles/5214735-digibeectl-use-guide).
```
curl -s https://storage.googleapis.com/digibee-release-test/releases/install.sh | bash
```
2) Configure digibeectl on your MAC or LINUX computer as described on [Digibeectl Official Documentation](https://intercom.help/godigibee/en/articles/5214735-digibeectl-use-guide).
```
digibeectl set config --file "path/file.json" --secret-key "encryption-key" --auth-key "encryption-passphrase"
```
3) Clone this repo on your MAC or LINUX computer
```
git clone https://github.com/arturscheiner/dgb-realmswitch.git
```
4) Access the cloned directory "dgb-realmswitch"
```
cd ./dgb-realmswitch
```
5) From inside the cloned directory, deploy this script in your $PATH. On this step the script will copy itself on the directory specified as a parameter. The directory must be a $PATH directory, otherwise you will not be able to run the command anywhere in your workstation, without the "./" in front of it.
```
sudo ./dgb-rs -d /usr/local/bin
```
6) Add the actual digibeectl configuration to the realm switch list.
```
dgb-rs -a
```
7) If you want to add another realm to the switch list, first unset the realm.
```
dgb-rs -u
```
8) After unsetting the realm as described above, repeat the steps 2 and 6.
   - Step 2 -> configure a new realm with digibeectl
   - Step 6 -> add the realm to the switch list
   
9) To get all of the realms in the switch list, run:
```
dgb-rs -l
```
10)  To switch between realms, just run:
```
dgb-rs -s realm-name
```
11) Get some HELP
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

### Obs: These two options just work when running ./dgb-rs inside the repo cloned folder.

```
about this script
c	Check this script deployment
	E.g. -> ./dgb-rs -c

d	Deploy this script into a directory
	E.g. -> sudo ./dgb-rs -d /usr/local/bin
```