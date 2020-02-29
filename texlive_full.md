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

   
   
2. if u simply run `sudo tlmgr update --self` it will throw:

   ```bash
   /usr/bin/tlmgr: Initialization failed (in setup_unix_one):
   /usr/bin/tlmgr: could not find a usable xzdec.
   /usr/bin/tlmgr: Please install xzdec and try again.
   tlmgr: Couldn't set up the necessary programs.
   Installation of packages is not supported.
   Please report to texlive@tug.org.
   Use of uninitialized value $r in split at /usr/share/texlive/tlpkg/TeXLive/TLUtils.pm line 4167.
   tlmgr: Cannot find main repository, you have to tag one as main!
   ```

   u basically have not initialised tlmgr usertree
   do that by: `tlmgr init-usertree`

3. still, this error might come:

   ```bash
   tlmgr: user mode database already set up in
   tlmgr:   /home/laferrari/texmf/tlpkg/texlive.tlpdb
   tlmgr: not overwriting it.
   ```

   now it is confirmed that you don't have **xzdec** installed, `sudo apt-get install xzdec`

4. ```bash
   Cross release updates are only supported with
     update-tlmgr-latest(.sh/.exe) --update
   Please see https://tug.org/texlive/upgrade.html for details.
   ```

   solution:

   ```bash
   # go to the link mentioned above
   # download the .sh script and run it
   ```

5. How i fixed my error?:
   I didn't. Just ensure that PATH variable contains the path for **texmf**, using `echo $PATH | grep tex`. 
   <font color="red">Note</font>: Use only the LateX workshop extension for vscode.