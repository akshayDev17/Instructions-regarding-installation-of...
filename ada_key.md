```bash
ssh-keygen
$ enter your custom file name

# copy key to server
ssh-copy-id -i <path/to/custom/file.pub> username@host

# test key
# use private key path
ssh -i <path/to/custom/file> username@host

# copy the generate public-private key pairs onto the server
cp <custom/file> <custom/file.pub> ~/.ssh

# test ssh again, it should work this time
```

