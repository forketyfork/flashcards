START
Basic
Front: 
How to check if an OpenSSH private key is passphrase-protected?
Back: 
Run: `ssh-keygen -y -f /path/to/private_key`
- `-y` means read the private key and print out the public key;
- `-f` specifies the file name;
- If prompted for a passphrase → Key is passphrase-protected;
- If public key displays immediately → Key has no passphrase.
<!--ID: 1745497011232-->
END
