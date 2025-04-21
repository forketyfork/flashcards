START
Basic
Front:
- What is swabra, what is its purpose, and how does it work? 
- How does it store its data?
- What are the options of this feature?
- What are the ignored directories?
- How to keep the swabra snapshot for debugging?
- How to avoid unnecessary clean checkouts?
Back: 

Swabra is a bundled TC plugin and respective feature that does the following:
- removes the files generated during the build; it creates a list of files in the checkout directory after source checkout and automatically removes the files not on this list after the build;
- detects modified/deleted files and report to the build log, allowing to make sure new builds don't start with files deleted or modified during the previous build, and initiate a clean checkout in this case;
- dumps processes that lock directory by the end of the build (requires handle.exe)

Swabra should be used only with automatic checkout mode, then it will run before first build set and record the file tree. It will store the directory state to the file `<hash>.snapshot` in the DiskDir format (existing files, last modification, size), the path to the checkout directory to be cleaned is stored to `snapshot.map` file.

- `filesCleanup` = `DISABLED,BEFORE_BUILD,AFTER_BUILD` — whether to clean up the files and when
- `forceCleanCheckout` — force clean checkout if the clean directory state can't be restored; if any files are deleted or modified, the clean checkout will be enforced; if this option is disabled, swabra will just display a warning;
- `paths`: a list of newline-separated paths to include (starting with `+:`) and exclude (starting with `-:`) from monitoring; the names are case-sensitive; should be specified according to their specificity: less specific rules should be placed above more specific; the first rule should always point to a directory;
- `lockingProcesses`: `DISABLED,REPORT,KILL` — whether to search for processes that lock checkout directory files and how to handle them (Windows only, requires SysInternals' `handle.exe` installation on the Administration -> Tools page, the build agent user should have administrator privileges)
- `verbose`: detailed logging;

If a build uses agent checkout, `.svn`, `.git`, `.hg`, `CVS` directories will be ignored; to disable this behavior, set `swabra.default.rules` configuration parameter to an empty value.

To keep the snapshot, set the `swabra.preserve.snapshot` setting.

To avoid unnecessary clean checkouts, identical Swabra build features have to be set for build configurations working in the same checkout directory (either having the same custom checkout directory path or the same VCS settings).

See:
- [Swabra](https://www.jetbrains.com/help/teamcity/kotlin-dsl-documentation/buildFeatures/swabra/)
- [Build Files Cleaner (Swabra) | TeamCity On-Premises Documentation](https://www.jetbrains.com/help/teamcity/build-files-cleaner-swabra.html)
<!--ID: 1745135900083-->
END
