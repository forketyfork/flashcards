START
Basic
Front: How to properly run alpine package manager in a Dockerfile?
Back: 
Run it with `--no-cache` parameter. This saves the trouble of running `apk update` before installation and `rm -rf /var/cache/apk/*` after:
```sh
apk add --no-cache curl
```
<!--ID: 1713345275201-->
END
