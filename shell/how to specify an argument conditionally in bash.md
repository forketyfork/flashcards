START
Basic
Front: In bash, how to specify an argument to a command based on a condition, using an alt value? What are the different forms of alt values?
Back: 
Use the following approach:
```shell
debug=""
[[ $1 == "--trace-commands" ]] && debug="yes"
bash ${debug:+"-x"} script
```

The `${debug:+"-x"}` form will produce a `"-x"` value only if the `debug` variable is set and not empty. If you want to check if it's set at all (even if empty), use the form `${debug+"-x"}`.
<!--ID: 1710309440242-->
END
