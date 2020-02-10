1. use the `ssh-keygen -t rsa -b 4096` to generate a private-public key pair.
2. open github.com, go to settings, SSH AND GPG keys.
3. copy the contents of public key file(extension = .pub) into key-section(textbox)
4. check the box(if you want read AND write permissions)
5. click add key
6. `eval "$(ssh-agent -s)"`
7. `ssh-add key_github`
8. `ssh -T -p 443 git@ssh.github.com` (we can remove -p 443, since this is the argument for the port)
9. `git remote set-url origin ssh://git@ssh.github.com:443/akshayDev17/NNprojects.git`
   instead of NNprojects.git, use your desired repo-name.
10. `sudo ufw disable` , use this if login is still disabled.



### reference links:

* https://stackoverflow.com/questions/8588768/how-do-i-avoid-the-specification-of-the-username-and-password-at-every-git-push
* https://askubuntu.com/questions/610940/ssh-connect-to-host-github-com-port-22-connection-refused
* https://stackoverflow.com/questions/7953806/github-ssh-via-public-wifi-port-22-blocked/34444860#34444860