START
Basic
Front: What types of dependencies are there between build configurations?
Back: 
There are two types of dependencies:  

- An _artifact dependency_ is a way to get artifacts produced by one build into another. Without a corresponding _snapshot dependency_, it is mainly used when the **build configurations are not related in terms of sources**. For example, one build provides a reusable component for others.
- A _snapshot dependency_ influences the way builds are processed and implies that **the builds are deeply related**, one build being a logic part of another. It expresses source-level dependencies and allows splitting a single monolith build into a build chain. The build structure is described declaratively.

A build configuration may have both a snapshot and an artifact dependency on another build configuration.

See: [https://www.jetbrains.com/help/teamcity/dependent-build.html](https://www.jetbrains.com/help/teamcity/dependent-build.html)
<!--ID: 1745135900087-->
END
