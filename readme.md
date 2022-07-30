blossom [![Build Status](https://img.shields.io/github/checks-status/Im-Fran/blossom/master?label=build)](https://github.com/Im-Fran/blossom/actions) [![License](https://img.shields.io/badge/license-LGPL_v2.1-lightgrey.svg?style=flat)][LGPL v2.1] [![Gradle Plugin](https://img.shields.io/gradle-plugin-portal/v/cl.franciscosolis.blossom-extended)](https://plugins.gradle.org/plugin/cl.franciscosolis.blossom-extended)
=========
blossom is a Gradle plugin for performing source code token replacements in Java, Kotlin, Scala, and Groovy based projects. It is licensed under the [LGPL v2.1] license.

## Usage
Apply the plugin to your project.

```kotlin
plugins {
  id("cl.franciscosolis.blossom–extended") version "1.3.1"
}
```
> (Use the latest version available)

Replacements can be configured through the `BlossomExtension`.

### Global Replacement (all files)

Replacing all instances of the string `APPLE` (case-sensitive) with the string `BANANA`, in **all files**.

```kotlin
blossom {
  replaceToken("APPLE", "BANANA")
}
```

### Local Replacement (per-file)

Replacing all instances of the string `APPLE` (case-sensitive) with the string `BANANA` in the **specified file(s)**.

```kotlin
blossom {
  val constants = "src/main/java/org/example/application/Constants.java"
  replaceToken("APPLE", "BANANA", constants)
}
```

[LGPL v2.1]: https://choosealicense.com/licenses/lgpl-2.1/
