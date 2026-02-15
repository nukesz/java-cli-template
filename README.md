# Java CLI Template

Minimal Java CLI template using Gradle.

## Run

```bash
./gradlew run
```

## Build

```bash
./gradlew build
```

## Native Build

```bash
./gradlew nativeCompile
```

This uses the GraalVM Native Build Tools Gradle plugin.

Native binary output:
- `build/native/nativeCompile/java-cli-template`

## CI and Release

- `CI` (`.github/workflows/ci.yml`): runs on commit pushes and pull requests.
- `Release` (`.github/workflows/release.yml`): runs on tags matching `v*`, builds JAR + native binary, and publishes a GitHub Release.

Release trigger example:

```bash
git tag v1.0.0
git push origin v1.0.0
```
