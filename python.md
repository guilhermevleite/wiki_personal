## Print Code

> enscript -fCourier8 -h -L60 -2r -G -psaida.ps prog.py
> ps2pdf14 saida.ps saida.pdf

Portrait -r
Landscape -2r
To better print, keep code under 70 columns

## VirtualEnv

Do not install opencv via apt-get, install it via pip3 inside a virtualenv

Command workon cv to change into virtualenv cv
