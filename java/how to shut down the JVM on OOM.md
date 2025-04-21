START
Basic
Front: How do you shut down the JVM on OOM?
Back: 
By default, JVM doesn't shut down on OOM. But in Java 8u92, two new options have been added:
- `-XX:ExitOnOutOfMemoryError` — JVM terminates on first OOM;
- `-XX:CrashOnOutOfMemoryError` — JVM crashes and produces text and binary crash files.
<!--ID: 1745138723646-->
END
