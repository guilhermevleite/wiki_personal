## To create a symbolic link:

ln -s /path/to/file /path/to/symlink

## Startup with gnome-terminal

> Open: Startup Applications 
> Add 
> Name: Terminal 
> Command: gnome-terminal 
> Add

## Wireless driver
* (This didn't worked for me 5.0GHZ was still off) Install wireless broadcom driver on Macbook Pro mid 2012:

> sudo apt-get update
> sudo apt-get remove --purge bcmwl-kernel-source
> sudo rm /etc/modprobe.d/blacklist-bcm43.conf
> sudo apt-get install b43-fwcutter firmware-b43-installer
> echo "options b43 nohwcrypt=1" | sudo tee -a /etc/modprobe.d/b43.conf
> sudo modprobe b43

> sudo iw reg set SE
> sudo sed -i 's/^REG.*=$/&SE/' /etc/default/crda

Source: https://ubuntuforums.org/showthread.php?t=2319292
Source: https://ubuntuforums.org/showthread.php?t=2214110

## Fan Control

> sudo apt-get install lm-sensors
> sudo apt-get install fancontrol

> sudo sensors-detect
Answer YES to all questions

Check if it works:
> sensors

> sudo service module-init-tools restart
or
> sudo service kmod start

Install psensor:
> sudo apt-get install psensor
Execute:
> psensor

Configure fancontrol:
> sudo pwmconfig
or edit:
> /etc/fancontrol

Restart fancontrol:
> sudo service fancontrol restart
Start fancontrol on startup:
> sudo service fancontrol start

### Alternative

> sudo add-apt-repository ppa:mactel-support && sudo apt-get update
> sudo apt-get install macfanctld

* Configuration:
> /etc/macfanctl.conf
* Restart daemon:
> /etc/init.d/macfanctld

## Stop Suspending

sudo systemctl mask sleep.target suspend.target hibernate.target
hybrid-sleep.target

### Move random files to folder

> This will move 4 random files from the current folder into the
new one
> ls | shuf -n 4 | xargs -i mv {} path_new_folder

### Get Folder Size

du -h --max-depth=1 ./
