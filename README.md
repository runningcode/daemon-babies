# Gradle Daemon Babies

## Description
This sample project reproduces a bug where a second gradle daemon is spawned when hitting the sync button in Android Studio.
This happens when including a settings.gradle.kts file in the buildSrc directory.

## Repro steps

1. Kill all gradle daemons
2. File -> Sync Project with Gradle Files
3. Watch as two Gradle Daemons are spawned. (verify by typing `jps` in console)