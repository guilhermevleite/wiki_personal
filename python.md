## Print Code

> enscript -fCourier8 -h -L60 -2r -G -psaida.ps prog.py
> ps2pdf14 saida.ps saida.pdf

Portrait -r
Landscape -2r
To better print, keep code under 70 columns

## VirtualEnv

Do not install opencv via apt-get, install it via pip3 inside a virtualenv

Command workon cv to change into virtualenv cv

### Install VirtualEnv

#### Install PIP

> wget https://bootstrap.pypa.io/get-pip.py
> sudo python get-pip.py
> sudo apt-get update
> sudo apt-get install -y python3-pip

#### Install VirtualEnv and VirtualEnvWrapper

> sudo pip3 install virtualenv virtualenvwrapper

Add these to ~/.zshrc

> export WORKON_HOME=$HOME/.virtualenvs
> export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
> source /usr/local/bin/virtualenvwrapper.sh

Run:

> source ~/.zshrc

#### Using VirtualEnv

* Create environment:
> mkvirtualenv <name>
* Activate:
> workon <name>
* Deactivate:
> deactivate
* Delete:
> rmvirtualenv <name>

### Install OpenCV inside VirtualEnv

> mkvirtualenv cv -p python3
> pip3 install opencv-contrib-python
