# dgb-realmswitch
A small script to allow switching between Digibee realms


# 
# Small script to help "switch" between Digibee Realms
# using digibeectl.
# 
# When you use the "set config" parameters, digibeectl 
# creates a config.json file inside the "current user" 
# ~/.digibeectl folder. After configuring your first
# "realm-token" move to the directory:
# 
# Supose that you have already created your digibeectl token
# to get acces to the realm "training". Do the configuration
# as described in the digibeectl manual. Now let's go in the 
# config directory:
#
# cd ~/.digibeectl
# ls
#
# You should be seeing the config.json file inside the
# directory. Rename the file to the name-of-the-realm.config.json
# check the example:
#
# mv config.json training.config.json
# 
# Check the digibeectl configuration running:
#
# digibeectl get config
#  
# You will see that it is empty, in the "not configured" state.
# Now let's create another digibeectl token for a second realm. Ex: poc-dgb
# Repeat the steps to configure digibeectl with the new token and
# check the ~/.digibeectl directory. Now you will see two files:
#
# - config.json - the new configuration created with the new poc-dgb token 
# - training.config.json - the configuration created on the previous step
#
# Rename the new config.json token to poc-dgb.config.json using the:
# 
# mv config.json poc-dgb.config.json
# 
# Copy and paste this content to a new shell script file using vim or any other editor.
# 
# vim dgb-sw
#
# Give permissions for this file to run as an executable:
# 
# chmod +x ./dgb-sw
# 
# Run the script with the "realm-name" as a parameter from the path you've created it.
#
# ./dgb-sw training
#
# Sudo copy the script to a folder in your $PATH.
# check the path with:
#
# echo $PATH
#
# sudo cp ./dgb-sw /usr/local/bin
#
# Run the command without the "./"
#
# dgb-sw training
# dgb-sw poc-dgb