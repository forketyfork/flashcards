START
Basic
Front: 
On which object are project properties available? 
How to set them from the command line, system property or environment variable?
How to check the presence of a property and read it at configuration time? At execution time?
Back: 
Project properties are available on the `org.gradle.api.Project` object.

Properties can be set:
- from the command line using the `-P` / `--project-prop` option;
- via a system property: `org.gradle.project.foo=bar`;
- via an environment variable: `ORG_GRADLE_PROJECT_foo=bar`.

Accessing properties at configuration time:
- checking the presence of the property: `hasProperty("myProjectProp")`.
- reading the property (exception is thrown if not present): `property("myProjectProp")`.
- reading the property (`null` is returned if not present): `findProperty("myProjectProp")` or `properties["myProjectProp"]`.
- using Kotlin delegated properties: `val myProjectProp: String by project`. For optional properties, use the `String?` type.

Accessing a property at execution time:
```kotlin
tasks.register<PrintValue>("printValue") {
    // Eagerly accessing the value of a project property, 
    // set as a task input
    inputValue = project.property("myProjectProp").toString()
}
```

Reference: https://docs.gradle.org/current/userguide/project_properties.html
<!--ID: 1745136966264-->
END
