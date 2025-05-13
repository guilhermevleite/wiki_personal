# Compress
> gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook -dNOPAUSE -dBATCH  -dQUIET -sOutputFile=output.pdf paper.pdf

Options for -dPDFSETTINGS:
screen
ebook
printer
prepress
default

# Split pdf
> pdftk <input.pdf> cat 12-15 output <output.pdf>

# Merge pdf
> pdftk <input_1.pdf> <input_2.pdf> cat output <output.pdf>
