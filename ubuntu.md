* (This didn't worked for me 5.0GHZ was still off) Install wireless broadcom driver on Macbook Pro mid 2012:

> sudo apt-get update
> sudo apt-get remove --purge bcmwl-kernel-source
> sudo rm /etc/modprobe.d/blacklist-bcm43.conf
> sudo apt-get install b43-fwcutter firmware-b43-installer
> echo "options b43 nohwcrypt=1" | sudo tee -a /etc/modprobe.d/b43.conf
> sudo modprobe b43

> sudo iw reg set SE
> sudo sed -i 's/^REG.*=$/&SE/' /etc/default/crda

- Source: https://ubuntuforums.org/showthread.php?t=2319292
- Source: https://ubuntuforums.org/showthread.php?t=2214110
