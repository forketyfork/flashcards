START
Basic
Front: 
How can you make a bind mount read-only?
Back: 
Use a two-step mount:
```shell

mount --bind /source /target

mount -o remount,bind,ro /target

```
<!--ID: 1745215325338-->
END
