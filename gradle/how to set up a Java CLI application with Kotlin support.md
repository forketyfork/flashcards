START
Basic
Front: 
How do you set up a Java project, a Java CLI application or a Kotlin project?
Back: 
```kotlin
plugins {
    // Apply the application plugin to add support for building a CLI application
    iapplication

    // Apply the plugin which adds support for Java
    java

    // Apply the plugin which adds support for Kotlin/JVM
    kotlin("jvm") version "2.2.0"
}
```

Or, for Groovy:
```
plugins {
    id 'application'
}
```

You might also see an older way of doing the same:
```kotlin
apply plugin: "application"   // for Groovy DSL
apply(plugin = "application") // for Kotlin DSL
```
END
