# GradleForMe
Gradle is an open-source build automation tool that is designed for multi-project builds and supports multiple programming languages. It is often used for building, testing, and deploying software projects. Gradle uses a **Groovy** or **Kotlin-based DSL** (Domain-Specific Language) to define build scripts, making it flexible and expressive.

## Default name for build file 
build.gradle

## Basic build.gradle
```groovy
// Define the project and its properties
plugins {
    id 'java'
}

group 'com.example'
version '1.0-SNAPSHOT'

// Configure the source and target compatibility for Java
java {
    sourceCompatibility = JavaVersion.VERSION_11
    targetCompatibility = JavaVersion.VERSION_11
}

// Define project dependencies
repositories {
    mavenCentral()
}

dependencies {
    // Example dependency on the Apache Commons Lang library
    implementation 'org.apache.commons:commons-lang3:3.12.0'
}

// Define custom tasks or configurations if needed
task customTask {
    doLast {
        println "Executing custom task"
    }
}

// Define additional configurations or settings as necessary

```
In this example:  
The **plugins** block applies the Java plugin, which provides default configurations for Java projects.  
The **group** and **version** statements set the group and version of the project.  
The **java** block configures the Java plugin, setting the source and target compatibility to Java 11.  
The **repositories** block specifies the Maven Central repository for resolving dependencies.  
The **dependencies** block declares project dependencies. In this case, it includes an example dependency on the Apache Commons Lang library.  
The **task** block defines a custom task named customTask that, when executed, prints a message.  
