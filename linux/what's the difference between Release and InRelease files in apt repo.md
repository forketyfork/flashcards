START
Basic
Front: 
What's the difference between Release and InRelease files in a Debian apt repository?
Back: 
Release files contain meta-information about the distribution and checksums for the indices. The `Release` file is accompanied by the `Release.gpg` file that contains the signature. The `InRelease` file contains both the data and the signature, to avoid races when fetching those two files.
<!--ID: 1745139755255-->
END
