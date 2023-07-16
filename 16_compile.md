---
layout: page
title: Compile
#permalink: /about/
---


# Compile the source

Most likely, you don't need to compile the source yourself.
It is absolutely safe to skip to the next section.

## Supported operating systems

Java implements the "compile once, run everywhere" principle.
The same jar file (result of compilation) will run on **Windows, Mac OS X and Linux.**
In the same way, you can compile on any of these operating systems and get a jar that works everywhere.

## Build with Gradle

You need Java 13 to build it.

To build the project, you need to check the source out and execute in the project's directory the command:
```
./gradlew build
```

To run it, execute:
```
./gradlew run
```

At least, that's in theory.
If the above does not work, continue reading.


## How the source is organized

There is only one source file. Because of that, this program may be used as a Linux shebang script
(the UI will look a bit more ugly with text instead of icons, but everything will work).
The project uses no annotation-based Java extensions.
If you cannot compile the project, you can take that single Java file and create your own project for it.

The source is built with Java 13. You can use Java 8 to run the jar, but you need Java 13 to build the source.


### Gradle plugins

The project is build with Gradle, and the following Gradle plugins are used:
* `java` — as usual for Java applications
* `application` — as usual for Java applications; in addition, sets `-Xmx`, the amount of heap memory, to 8G
* `com.palantir.git-version` — lets the application know its version (via Implementation-Version in the manifest),
   the version number is shown in the bottom of the help window, "n/a" is shown there if the version number is unavailable
* `jacoco` — for test coverage, it absolutely safe to switch it off

### Resources

The only used type of resources is icons. There are many button icons and one application icon.
The application can work even without icons, an alternaive text will be shown.

### MANIFEST.MF

* `Manifest-Version` — as usual
* `Main-Class` — as usual
* `Implementation-Version` — the version is shown in the bottom of the help window; "n/a" is shown if the version number is unavailable

### Heap memory

The `-Xmx` parameter is set to 8G. This is required for the big Perseverance images that consist of 4, 12 or 16 parts, each part being the size of a normal image.

If you do not assemble big Perseverance images from parts, the default memory setting is ok.

This setting goes to the launching scrpts, `x3dview` and `x3dview.bat`.

### Unit tests

The source is covered with unit tests. Unlike the single-file source, tests use the traditional file-per-class approach.
The coverage digit has never been a goal. The code borrowed from free sources is usually not covered with tests.

## Build results

The file `x3dview.zip` will be created in the `build/distributions/` subdirectory of the project.



