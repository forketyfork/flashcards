START
Basic
Front: 
How do you define a Java version for the build?
Back: 
Add a JVM toolchain resolver plugin to the `settings.gradle.kts`:
```kotlin
plugins {
    id("org.gradle.toolchains.foojay-resolver-convention").version("1.0.0")
}
```

Specify the toolchain version in the java plugin configuration:
```kotlin
java {
    toolchain {
        languageVersion = JavaLanguageVersion.of(17)
    }
}
```
END
