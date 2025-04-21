START
Basic
Front: How to add a multiline env variable to a docker-compose file?
Back: 
```yaml
environment:
  - ENV1=abce
  - ENV2=asdf
  - |
    ENV_MULTILINE=
    Line1
    Line2
```
<!--ID: 1745138891619-->
END
