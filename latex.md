# Latex

### Required Packages

> sudo apt install texlive-latex-extra texlive-fonts-recommended texlive-science

Simplest case  
  
> latexmk
  
Will run latex on all .tex in the current folder

> latexmk -pdf

to get a pdf as output

> latexmk file.tex

to run on a specific file

> latexmk -pv

to preview the output file

> latexmk -pvc

to continously check for changes and recompile if needed to display the result

> latexmk -c

after done to clear temporary files

> latexmk -C

To clear .pdf .ps and .dvi took

Add this to ~/.latexmkrc

> $pdf\_previewer = 'start evince';

TLMGR is the package manager for latex

Change the repo to 2017 version, otherwise install the 2019, which god knows how it is done...
sudo tlmgr option repository ftp://tug.org/historic/systems/texlive/2017/tlnet-final

tlmgr update -all to update before anything
tlmgr install cite to install cite package
