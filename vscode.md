1. `sudo apt update`
2. `sudo apt install software-properties-common apt-transport-https wget`
3. `wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -`
4. `sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`
5. `sudo apt update`
6. `sudo apt install code`

