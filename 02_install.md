---
layout: page
title: Install/Run
#permalink: /about/
---


# Install and/or run

## Make sure you have Java

First of all, you must have Java. It must be at least Java 8. It is likely that your computer already has some version of Java installed.
To check the version of Java, please execute in the command line[^cmdl]:
```
java -version
```

You will see something like:
```
me@comp:~$ java -version
openjdk version "13.0.7" 2021-04-20
OpenJDK Runtime Environment (build 13.0.7+5-Ubuntu-0ubuntu120.04)
OpenJDK 64-Bit Server VM (build 13.0.7+5-Ubuntu-0ubuntu120.04, mixed mode)
me@comp:~$ 
```
In this case we see Java 13, it is ok[^pre8].

## Run without installation

Run
```
java -version
```
from the command line. You must see a message telling you the version of Java, and that version must be at least 8. (Well, 1.8 is the same as 8[^sver].)

Download x3dview.zip, open the archive, and unpack the file x3dview.jar to some directory.

In the command line, go to that directory and run
```
java -jar x3dview.jar
```
You will see some messages, and then a window will open with two similar but different images.


under construction

prev: {{page.previous.url}}


next: {{page.next.url}}

this:{{page.url}}

-------------------

[^cmdl]: "Command line", also known as "Command Prompt", "Console", or "Terminal" is a very old way of interacting with a computer.
    This program behaves like an electric typewriter attached to a (very old) computer. It lets you type in text by pressing keys,
    and lets you see what the computer prints. You type in a command, press "Enter" (a.k.a. "Return"), and the computer executes
    your command. If you press Control+C, the computer will _Cancel_ what it is doing (yes, "Cancel", not "Copy", stop doing without
    caring to complete).

[^sver]: There is "Semantic Versioning", an approach to giving version numbers to software. According to Semantic Versioning, you
    increment the leftmost number when you break the existing API. If you cannot allow yourself to break the existing API and
    thus cause problems for your customers, you cannot change the leftmost number. But from the marketing perspective, you have to
    increment that number each time you add new features, so they advertised 1.2 as 2 and 1.5 as 5. Afer that they could not increment
    the leading 1 anymore. Although Java started with semantic versioning, they did not increment the leftmost 1 even after
    making incompatible changes; Java does not use the Semantic Versioning since Java 9, now (in 2023) there is no leading 1, and the 2nd number is always 0.

[^pre8]: If you see a Java version number less than 8 (or 1.8) in 2023, there must be a reason for it. Note that it is possible to
    have multiple versions of Java on the same computer and use them all, so maybe there still is a newer version of Java.
    If there is one, you can use it e.g. by specifying the full path, for example,
    ```
    /usr/lib/jvm/java-17-openjdk-amd64/bin/java -jar x3dview.jar
    ```
    One possible reason for having an old Java is having some old software that requires that old Java: in theory, Java 8 had
    to be backward-compatible with Java 6, but that's only in theory; if you replace the default Java, you may break such software.
    One more concern is disk memory: a computer with Java 6 on it is likely to have no free room on its hard disk in 2023.
