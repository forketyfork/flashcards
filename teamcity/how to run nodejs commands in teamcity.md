START
Basic
Front: 
How do you run NodeJS commands in TeamCity builds? How to use a private registry for such step?
Back: 
Use the `nodeJS` build runner. It will run the build in a Docker container from the `node:lts` image by default (can be adjusted with a `dockerImage` parameter, or detected from the `.nvmrc` file):

```kotlin
buildType {
    steps {
        nodeJS {
            name = "Node.js test"
            workingDir = "frontend"
            shellScript = """
                npm ci
                npm run test
            """.trimIndent()
            dockerImage = "node:18"
        }    
    }
}
```

To use a private npm registry inside this step, configure the registry on the project level:

```kotlin
project {
    buildType(Build)

    features {
        npmRegistry {
            id = "PRIVATE_REGISTRY"
            name = "NPM Registry"
            scope = "scope" // empty to override default registry
            token = "credentialsJSON:xxx"
        }
    }
}
```

And add a reference to it to the build type:

```kotlin
object Build : BuildType({
    features {
        npmRegistry {
            connectionId = "PRIVATE_REGISTRY"
        }
    }
}
```

As an alternative, add a password parameter:
```kotlin
params {
	password("env.NPM_TOKEN", "credentialsJSON:...")
}
```

And add the following to your project's `.npmrc` file:
```
//registry.npmjs.org/:_authToken=${NPM_TOKEN}
```

See:
- [Node.js | TeamCity On-Premises Documentation](https://www.jetbrains.com/help/teamcity/nodejs.html)
- [NodeJSBuildStep](https://teamcity.jetbrains.com/app/dsl-documentation/buildSteps/node-j-s-build-step/index.html)
- [NpmRegistryConnection](https://teamcity.jetbrains.com/app/dsl-documentation/projectFeatures/npm-registry-connection/index.html)
<!--ID: 1745135900085-->
END
