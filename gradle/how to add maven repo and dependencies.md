START
Basic
Front: 
How do you add a maven repository to your project (e.g., maven.google.com) and specify some dependencies, like junit and guava?
Back: 
```kotlin
repositories {
    google()
}

dependencies {
    testImplementation("junit:junit:4.13.2")
    implementation("com.google.guava:guava:33.4.8-jre")
}
```
END
