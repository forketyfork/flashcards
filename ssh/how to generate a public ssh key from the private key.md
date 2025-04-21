START
Basic
Front: How to generate a public ssh key from the private key?
Back: 
Use the following command:
```sh
ssh-keygen -f id_rsa -y
```

If it complains about permissions, change them to proper ones:
```
chmod 600 id_rsa
```
<!--ID: 1745139815769-->
END
