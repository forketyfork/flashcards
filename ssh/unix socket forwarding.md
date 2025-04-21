START
Basic
Front: How to allow Unix-domain socket forwarding for the sshd?
Back: 
Use the property `AllowStreamLocalForwarding=yes(default)/all/local/remote/no`. The `local` value allows only the local (from the ssh client PoV) forwarding of StreamLocal, `remote` allows only remote forwarding, `yes/all` allow both.
<!--ID: 1745139815761-->
END
