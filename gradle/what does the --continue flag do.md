START
Basic
Front: 
What does `--continue` flag mean for the Gradle build?
Back: 
The `--continue` flag in Gradle allows the build to continue executing tasks even after a task failure occurs. By default, Gradle stops execution as soon as any task fails. When the `--continue` option is used, Gradle will:
* Execute all tasks whose dependencies have completed successfully, skipping only the tasks that depend on failed ones.
* Report all encountered failures at the end of the build.
<!--ID: 1745222218938-->
END
