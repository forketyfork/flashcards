START
Basic
Front: 
How do you define a Java CLI application in a Gradle build? How do you run it using Gradle?
Back: 
```kotlin
plugins {
    application
}

application {
    mainClass = "HelloWorld"
}

tasks.jar {
    manifest {
        attributes("Main-Class" to "Helo")
    }
}
```

- run it using `gradle run`
- build a jar using `gradle jar`, the jar will be located at `build/libs`.
END
