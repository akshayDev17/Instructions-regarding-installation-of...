## Command:

`sudo apt-get install texlive-full`

# probable errors and their resolve:

1. ```bash
   dpkg: error processing archive /var/cache/apt/archives/texlive-fonts-extra-doc_2018.20180505-1~16.04.york0_all.deb (--unpack):
    trying to overwrite '/usr/share/doc/texlive-doc/latex/mweights/README', which is also in package texlive-latex-extra-doc 2015.20160320-1
   ```

   solution:

   ```bash
   # force dpkg to overwrite the above mentioned README by:
   sudo dpkg -i --force-all /var/cache/apt/archives/texlive-fonts-extra-doc_2018.20180505-1~16.04.york0_all.deb
   ```

   