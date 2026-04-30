# Renetik Android Testing

[![Android Build](https://github.com/renetik/renetik-android-testing/actions/workflows/android.yml/badge.svg)](https://github.com/renetik/renetik-android-testing/actions/workflows/android.yml)

Shared Android test dependencies and helpers for Renetik Android libraries.

## Installation

Add JitPack to dependency resolution:

```gradle
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```

Add the testing artifact to test dependencies:

```gradle
dependencies {
    testImplementation 'com.github.renetik:renetik-android-testing:1.0.0'
}
```

## Compatibility

- Java: 21
- Gradle wrapper: 9.4.1
- Android Gradle Plugin: 9.2.0
- Kotlin: 2.3.21
- compileSdk: 36
- minSdk: 26

## Included Test Dependencies

- JUnit 4
- MockK
- Robolectric
- kotlinx-coroutines-test

## Release

Publishable builds use the release Android variant with a sources jar:

```sh
./gradlew clean build publishToMavenLocal --no-daemon
```
