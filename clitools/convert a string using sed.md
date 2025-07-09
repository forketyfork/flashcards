START
Basic
Front: 
Take a string `251.14886` and make `2025.1` out of it using sed.
Back: 
```shell
echo "251.14886" | sed -r 's/(..)(.*)\..*/20\1.\2/'
```

**Explanation:**
- `(..)` captures first 2 characters ("25") as group 1
- `(.*)` captures remaining characters before the dot ("1") as group 2  
- `\..*` matches the dot and everything after (discarded)
- `20\1.\2` replaces with: "20" + group1 + "." + group2 = "2025.1"

**General pattern:** `s/pattern/replacement/` with capture groups `()` and backreferences `\1`, `\2`, etc.
<!--ID: 1745238713672-->
END