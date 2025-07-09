START
Basic
Front: 
Take a string `251.14886` and make `2025.1` out of it using awk.
Back: 

```shell
echo "251.14886" | awk '{ print "20" substr($1, 1, 2) "." substr($1, 3, 1) }'
```

**Explanation:**
- `substr($1, 1, 2)` extracts characters 1-2 ("25")
- `substr($1, 3, 1)` extracts character 3 ("1") 
- String concatenation: "20" + "25" + "." + "1" = "2025.1"

**General pattern:** `substr(string, start_position, length)` extracts substrings for manipulation
<!--ID: 1745480658577-->
END