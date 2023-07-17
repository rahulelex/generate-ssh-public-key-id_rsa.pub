# Generate SSH Public Key id_rsa.pub
Many Git servers authenticate using SSH public keys. Ensure that the id_rsa.pub file does not exist in the ~/.ssh directory.
### Step 1: Go to the ssh directory
```sh
$ cd ~/.ssh
```
### Step 2: Generate SSH key
```sh
$ ssh-keygen -o
```
Output is
```sh
Generating public/private rsa key pair.
Enter file in which to save the key (/home/rahul/.ssh/id_rsa):
Created directory '/home/rahul/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/rahul/.ssh/id_rsa.
Your public key has been saved in /home/rahul/.ssh/id_rsa.pub.
The key fingerprint is:
d0:82:24:8e:d7:f1:bb:9b:33:53:96:93:49:da:9b:e3 rahul@mylaptop.local
```
- First it confirms where you want to save the key (.ssh/id_rsa), and then it asks twice for a passphrase, which you can leave empty if you don’t want to type a password when you use the key. However, if you do use a password, make sure to add the -o option; it saves the private key in a format that is more resistant to brute-force password cracking than is the default format. You can also use the ssh-agent tool to prevent having to enter the password each time.

### Step 3: Copy the entire content of .pub file to utilize it as a public key wherever needed.
```sh
cat ~/.ssh/id_rsa.pub
```
Output is
```sh
ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
NrRFi9wrf+M7Q== rahul@mylaptop.local
```
## License
**Free Software, Hell Yeah!**

## Authors
- [Rahul Gupta](https://github.com/rahulelex)
