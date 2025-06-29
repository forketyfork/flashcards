START
Basic
Front: 
Take a string `251.14886` and make `2025.1` out of it using awk.
Back: 

```shell
echo "251.14886" | awk '{ print "20" substr($1, 1, 2) "." substr($1, 3, 1) }'
```
<!--ID: 1745480658577-->
END