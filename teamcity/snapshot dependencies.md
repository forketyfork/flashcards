START
Basic
Front: What does a snapshot dependency ensure? How does the revision synchronization setting affect the snapshot dependency? How does a snapshot dependency alter the build behavior? Which options are available for the behavior of the build on snapshot dependency failure? How to reference parameters of preceding builds or parameters pushed down the snapshot dependency chain? What is the recommended way of triggering the chain builds?
Back: 
A snapshot dependency of build configuration A on build configuration B means that each build of A has a "suitable build" of B before it can start.   
  
Depending on the revision synchronization:  

- if the **revision synchronization is enforced**, then both builds will use the same source snapshot (if the VCS root is the same, it will be the same revision, otherwise it will be revisions taken at the same moment in time);
- if the **revision synchronization is not enforced**, then build A can use up-to-date revisions when promoting a finished build B to A.

A snapshot dependency alters the build's behavior as follows:  

- when a build is queued, all of its snapshot dependencies are also queued, and their revisions are determined;
- if some snapshot dependency build configuration already has a started build with matching changes ("suitable build"), and this dependency has _"Do not run new build if there is a suitable one"_ option set to ON, TeamCity optimizes the builds by reusing the suitable ones and silently removing the duplicate builds from the queue;
- the snapshot dependencies start on the explicitly set revisions defined as per to the **revision synchronization** setting (see above);
- if the snapshot dependency is also an artifact dependency with the _"Build from the same chain"_ option enabled, TeamCity ensures that the artifacts will be downloaded from this dependency;
- builds that are part of a build chain are preserved from clean-up by default.

In case of the snapshot dependency build failure, there are the following options:  

- **run build, but add problem** - the build will run, but will be marked as failed;
- **run build, but do not add problem** - the build will run with no problems added;
- **mark build as failed to start** - the build will not run and will be marked as "Failed to start";
- **cancel build** - the build will not run and will be marked as "Canceled".

Referencing parameters from the preceding builds: `dep.<configurationId>.<parameterName>`

Referencing parameters pushed down the chain: `reverse.dep.<configurationId>.<parameterName>`

When setting up the triggers, think about the result, what you want to get at the end of the process. Set up the triggers only for the top level build. The snapshot dependencies normally don't need to be triggered, they will be added to the queue automatically.

See [https://www.jetbrains.com/help/teamcity/dependent-build.html#Snapshot+Dependency](https://www.jetbrains.com/help/teamcity/dependent-build.html#Snapshot+Dependency)
<!--ID: 1745135900084-->
END
