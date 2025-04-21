START
Basic
Front: 
How to get the current number of milliseconds passed since the Epoch, in UTC?
Back: 
```
Instant.now().toEpochMilli()
```
The `Instant.now()` method obtains the current instant from the system UTC clock. The `Instant.toEpochMilli()` method will convert it to the number of milliseconds passed from the epoch of `1970-01-01T00:00:00Z`.
<!--ID: 1745138723649-->
END
