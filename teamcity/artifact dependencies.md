START
Basic
Front: What is an artifact dependency? What will happen if I add a dependency both as a snapshot dependency and an artifact dependency? How does artifact dependency affect cleaning of the artifacts?
Back: 
Artifact dependency allow to use the output (artifacts) of one build in another build. The artifacts are downloaded to the agent when a build starts.   

If the dependency is both snapshot and artifact, then the _"Build from the same chain"_ option must be set for it to download the results from the build with the same sources. 
  
If the build's artifacts were downloaded by other builds which were not yet cleaned up, then they may not be cleaned from this build either. For a dependent build, there's a setting to clean the artifacts downloaded from the other build.  
  
See [https://www.jetbrains.com/help/teamcity/dependent-build.html#Artifact+Dependency](https://www.jetbrains.com/help/teamcity/dependent-build.html#Artifact+Dependency)
<!--ID: 1745135900088-->
END
