START
Basic
Front: 
How to enter the ssh console and forward a port in an existing ssh connection?
Back: 
Run the ssh command with the `-o EnableEscapeCommandline=yes` key, then press `~C` in the terminal window. You should see the `ssh>` prompt where you can enter a port forwarding command like `-R 8080:localhost:8080`.
<!--ID: 1745214796384-->
END
