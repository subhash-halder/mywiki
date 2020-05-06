### backup gpg key

```
# to get the key id

$ gpg --list-keys --keyid-format long

/home/user/.gnupg/pubring.gpg
--------------------------------
pub rsa4096/ABCDFE01 2020-04-28
uid firstname lastname (description) <email@example.com>
sub rsa4096/DEFABC01 2020-04-28
```


### get the public and private key to a file
```
$ gpg --output mygpgkey_pub.gpg --armor --export ABCDFE01
$ gpg --output mygpgkey_sec.gpg --armor --export-secret-key ABCDFE01
```

zip it and save it in a safe place


### importing the gpg key

```
$ gpg --import ~/mygpgkey_pub.gpg
$ gpg --allow-secret-key-import --import ~/mygpgkey_sec.gpg


# run the list command to see the key

$ gpg --list-keys --keyid-format long

/home/user/.gnupg/pubring.gpg
--------------------------------
pub rsa4096/ABCDFE01 2020-04-28
uid firstname lastname (description) <email@example.com>
sub rsa4096/DEFABC01 2020-04-28

```
