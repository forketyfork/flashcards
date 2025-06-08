START
Basic
Front: 
If you have `set -u` and want to check some variable that may not be defined, how to do that?
Back: 
`set -u` means treat unset variables as errors, so you can't check for the existence of a variable, e.g., `[ -z "$MYVAR" ]`, without failing the script. To avoid this, add the following to the top of the script:
```shell
: "${MYVAR:=}"
```

`:` is a no-op command that always succeeds, `${MYVAR:=}` sets the variable to an empty string if it's unset.
END
