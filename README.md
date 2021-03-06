<p align="center">
  <a href="https://www.instagram.com/devfullcycle/" target="blank"><img src="https://fullcycle.com.br/wp-content/themes/fullcycle-blog/application/img/logo-fullcycle.png"/></a>
</p>

# Script to enable systemd in WSL2 (Ubuntu/Debian)

Script to enable systemd support on current Ubuntu WSL2 images from the Windows store. 
Tested on 18.04, 20.04 and the versionless (current) version of Ubuntu from the Windows Store.
I am not responsible for broken installations, fights with your roommates and police ringing your door ;-).

*Note: I don't have the right tools to test/chagne this script at the moment. I you like to be an active maintainer, testing out PR's and updating code when necesary, please mail me (see profile). 

Instructions from [the snapcraft forum](https://forum.snapcraft.io/t/running-snaps-on-wsl2-insiders-only-for-now/13033) turned into a script. Thanks to [Daniel](https://forum.snapcraft.io/u/daniel) on the Snapcraft forum! 

## Install
You need ```git``` to be installed for the commands below to work. Use
```sh
sudo apt install git
```
to do so.
### Run the script and commands
```sh
git clone https://github.com/DamionGans/ubuntu-wsl2-systemd-script.git
cd ubuntu-wsl2-systemd-script/
bash ubuntu-wsl2-systemd-script.sh
# Enter your password and wait until the script has finished
```
### Then restart the Ubuntu shell and try running systemctl
```sh
systemctl
```
If you don't get an error and see a list of units, the script worked.

## Configure on Bash

Add this line on top the .bashrc or the .zshrc (zsh/oh-my-zsh):
```sh
source /usr/sbin/start-systemd-namespace
```
In .bashrc or zshrc (oh-my-zsh)

Have fun using systemd on your Ubuntu WSL2 image. You may use and change and distribute this script in whatever way you'd like. 
