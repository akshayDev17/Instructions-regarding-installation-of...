# Installing offline dictionary for Ubuntu

```bash
sudo add-apt-repository "deb http://archive.ubuntu.com/ubuntu $(lsb_release -sc) universe"
sudo apt-get install dict
sudo apt-get install dictd
```



Since the dictionary only has the **dummy** database at this point, we need to install more databases

```
sudo apt-get install dict-gcide
sudo apt-get install dict-wn
sudo apt-get install dict-devil
```



## Usage

use ```dict -D``` to check available databases.

for thesaurus database:

```sudo apt-get install dict-moby-thesaurus```

to view from a particular database(for eg. word-net[wn]) :

```dict -d wn "dictionary"```

to view from all databases :

```dict "dictionary"```



[Reference link](https://askubuntu.com/questions/170775/offline-dictionary-with-pronunciation-and-usages)

