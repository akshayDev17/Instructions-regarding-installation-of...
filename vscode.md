## install vscode

1. `sudo apt update`
2. `sudo apt install software-properties-common apt-transport-https wget`
3. `wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -`
4. `sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`
5. `sudo apt update`
6. `sudo apt install code`



## Configure java jdk for vscode

```bash
# get the openjdk-11
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt install openjdk-11-jdk
```

Open vscode, install the extensions [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java) and [VS intellicode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode) .

Open user settings.json by

1. open the command palette using `Ctrl+Shift+P`

2. type settings.json, and choose `Preferences: Open Settings(JSON)`

3. ```json
   "java.configuration.runtimes": [
           {
             "name": "JavaSE-1.8",
             "path": "path/to/jdk-8",
           },
           {
             "name": "JavaSE-11",
             "path": "path/to/jdk-11",
           },
         ]
   ```



the paths can be found in the directory `/usr/lib/jvm/` 

refer [this link](https://marketplace.visualstudio.com/items?itemName=redhat.java#setting-the-jdk) for more