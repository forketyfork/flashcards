START
Basic
Front: 
How to exclude packages from the installation by `apt-get install` command? How to include packages?
Back: 
From `man apt-get`:
If a hyphen is appended to the package name (with no intervening space), the identified package will be removed if it is installed. Similarly a plus sign can be used to designate a package to install. These latter features may be used to override decisions made by apt-get's conflict resolution system.

END
