# PS3 controller on Ubuntu:

### Installing

> sudo apt-get install dialog build-essential pyqt4-dev-tools libusb-dev libbluetooth-dev python-dbus pkg-config -y  
> wget https://github.com/RetroPie/sixad/archive/master.zip -O sixad-master.zip  
> unzip sixad-master.zip  
> cd sixad-master  
> make  
> sudo make install  

### Configuring

* First make sure you have Bluetooth on your computer.

* Plug in the controller via USB first to do the initial pairing.
  * Run the sixpair command:
    * > sudo sixpair

Sample of output when successful pair:

> Current Bluetooth master: XX:XX:XX:XX:XX:XX  
> Setting master bd_addr to XX:XX:XX:XX:XX:XX  

XX:XX:XX:XX:XX:XX is the MAC of your Bluetooth device.

* Unplug the controller and run:

> sudo sixad -s

 * This starts the sixad daemon which waits for incoming PS3 controller connections. sixad will completely take over the Bluetooth adapter (exclusive control, so no other Bluetooth devices other than PS3 controllers will work after you start sixad).

* Press the ps3 button on your PS3 controller and wait for 2-3 seconds. You’ll feel the controller vibrate when it successfully connects.

Sample of output when successful connected:

> [ ok ] Starting bluetooth (via systemctl): bluetooth.service.  
> sixad-bin[23052]: started  
> sixad-bin[23052]: sixad started, press the PS button now  
> Watching... (5s)  
> sixad-sixaxis[23069]: started  
> sixad-sixaxis[23069]: Connected 'PLAYSTATION(R)3 Controller (XX:XX:XX:XX:XX:XX)' [Battery 05]  

To turn off sixad and disable the controller:

Just press CTRL+C<Paste>
