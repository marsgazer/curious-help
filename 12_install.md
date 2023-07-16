---
layout: page
title: Install/Run
#permalink: /about/
---


# Install and/or run

Note that `x3dview` does not need installation. It can run from any directory (any folder, if you prefer this parlance).
It does not use any directories, hidden or not, to  store any data. No cache directory. No garbage on the hard disk.

It does not assume that your hard disk is infinite. You can install Ubuntu on a 32G USB stick and run `x3dview` from it.

## Make sure you have Java

Whether you prefer to install `x3dview` or run it without installing,
first of all, you must have Java. It must be at least Java 8. It is likely that your computer already has some version of Java installed.
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

## Run without installation (Windows, Mac OS X, Linux)

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

Video: download and run (no sound)

https://github.com/marsgazer/curious-help/assets/101140007/19118ffc-8f46-4214-a1f7-b305f0a79bef

<div class="embed-container">
  <iframe
      src="https://github.com/marsgazer/curious-help/assets/101140007/19118ffc-8f46-4214-a1f7-b305f0a79bef"
      width="700"
      height="480"
      frameborder="0"
      allowfullscreen="true">
  </iframe>
</div>


## Run from the source without installation

Starting from Java 11, you can run any single-file program just from the source, providing the path if necessary:

```
java Main.java

java src/main/java/com/github/martianch/curieux/Main.java

/usr/lib/jvm/java-13-oracle/bin/java src/main/java/com/github/martianch/curieux/Main.java
```

The file Main.java can be downloaded from the source tree of this project:
[direct link](https://raw.githubusercontent.com/martianch/curieux/master/src/main/java/com/github/martianch/curieux/Main.java).
In the worst case you will have to copy and paste the whole source into the text editor.
(Yes, this software is a single-file program. Running from source is a feature that I do not want to drop.)

There are two disadvantages: the icons will not be available and the UI will look rather ugly, icons on buttons will be replaced with text;
the startup time will include the time necessary to compile the code.
Unless you have to have a reason to use namely this method, please consider running from a `.jar`.

## Running as a script

One more option is to use it as a shebang script, if you know what shebang (`#!`) does in `sh` and/or `bash`.
You will have to copy the file `Main.java` to some other file name like `curious` or `x3view` (the script will not work with the extension `.java`),
uncomment the shebang in the first line of the script file, allow execution of that file (`chmod a+x curious`),
and place that script file in some directory that's already in the path (you do know what $PATH is, don't you?).

There are two disadvantages: the icons will not be available and the UI will look rather ugly, icons on buttons will be replaced with text;
the startup time will include the time necessary to compile the code.
Unless you have to have a reason to use namely this method, please consider running from a `.jar`.

## Install under Linux

First of all, you need Java. But I assume you have already tried to run this software wthout installation, and so you already do have Java.

Download x3dview.zip from the latest [release](https://github.com/martianch/curieux/releases) to your `Downloads` directory (`~/Downloads`, the tilde means "my home directory",
the directory will likely have a different name if you use a language other than English).
Note that if the file already exists, the browser will likely try to rename it to something like `x3dview (1).zip`,
so that the latest version will be `x3dview (1).zip` rather than `x3dview.zip`.
Do the following in the terminal:

```
cd /opt
sudo mkdir x3dview
sudo chmod a+rwx x3dview
unzip -o ~/Downloads/x3dview.zip
```

You will get the following directory structure:

```
/opt$ tree x3dview/
x3dview/
├── bin
│   ├── x3dview
│   └── x3dview.bat
└── lib
    └── x3dview.jar

2 directories, 3 files
```

From now on you can run `x3dview` from the terminal via `/opt/x3dview/bin/x3dview`, but let's add it to the path.

```
cd /usr/bin
sudo ln -s /opt/x3dview/bin/x3dview x3dview
```

Now you can run it just as:
```
x3dview
```

Let's add it to the launcher (invoked via the "Windows" key on the keyboard, the one between Fn and Alt).
Create the file `~/.local/share/applications/x3dview.desktop` with the following contents:

```
[Desktop Entry]
Type=Application
Name=Curious: X3D Viewer
#Icon=/full/path/xxx.svg
# !!! specify the correct path below !!!
Exec="/opt/x3dview/bin/x3dview" %F
Comment=View Images as Stereo Pairs
Categories=Graphics;2DGraphics;3DGraphics;RasterGraphics;Viewer;
Terminal=false
```


After that, you will be able to select one or two image files, click the right mouse button on the selection,
select "Open With Other Application" from the menu, click "View All Applications" if the application is not in the list,
select "Curious: X3D Viewer", and have the application run.

If you specify `Terminal=true` in the last line of that file, you will see the debugging output.

## Install under Mac OS X


**Disclaimer:** need to proofread this section. It's been a while since I used a Mac OS X.

First of all, you need Java. But I assume you have already tried to run this software wthout installation, and so you already do have Java.

Download x3dview.zip from the latest [release](https://github.com/martianch/curieux/releases) to your `Downloads` directory (`~/Downloads`, the tilde means "my home directory",
the directory will likely have a different name if you use a language other than English).
Note that if the file already exists, the browser will likely try to rename it to something like `x3dview (1).zip`,

Unpack the `x3dview.zip` file. In its `bin/` subdirectory you will find the script `x3dview`.

Basically, Mac OS X is a bit paranoid: by default it will not let you run the script `x3dview` downloaded from Internet.
This is because this is free software, and they want you to use paid software, and they want the developers to pay them for signing the software.
What can you do?

1. Open the file `xdview` with a text editor, select all text and copy it to the clipboard, create a new file, paste the text,
    save the file as `x3dview1`. Remove `x3dview`, rename `x3dview1` to `x3dview`. Make the file executable:
    ```
    chmod a+x x3dview
    ```
    Now it's you who created that script!

2. Alernatvely, you can do that via the command line:
    ````
    cat x3dview >x3dview1
    rm x3dview
    mv x3dview1 x3dview
    chmod a+x x3dview
    ````
    Now it's you who created that script!

What does the script do? It locates the `x3dview.jar` file and specifies the amount of heap memory for Java. Running
the script `x3dview` from any folder is a bit more convenient than running it from the folder containing the `x3dview.jar`
file and specifying `-Xmx8G` on the command line.

## Install under Windows

`x3dview` does not require instalation, it can run from any directory. On the other hand, having it in the UI among other applications may be convenient.

Download `x3dview.zip` from the latest release, open the zip archive, extract all. Now you will have the subfolder `x3dview` in your `Downloads` folder.
Navgate to that `x3dview` folder and then to `bin` in it. Click on `x3dview.bat`.

You will likely see some message of the sort: "Windows protected your PC, prevented an unrecognized app from starting".
Do not click the "Don't run" button yet! There is a "More info" link, click it. Now the button "Run anyway" appears, click it.


If the above does not work, your case is different, and Windows does not let you run `x3dview.bat` because it is downloaded from the Internet, do the following
(yes, I know this sounds paranoid):
Launch Notepad, select File-Open in the menu, navigate to `Downloads`  `x3dview`  `x3dview`  `bin`, you will see "No items match your search" and no files,
click the control that reads "Text Documents (*.txt)" in the bottom right-hand corner and select "All Files (*.*)" instead. Select `x3dview.bat`.
Select all text and copy it to the clipboard (Ctrl+A, Ctrl+C). Open a new Notepad window and paste the text from the clipboard (Ctrl+V).
Select File-Save in the menu, check that you are going to save to the same folder (select "All Files (*.*)" to see x3dview.bat in that folder).
Type a different file name, e.g. `x3dview1.bat` or `curious.bat`. Close Notepad (both windows). You will see the new file in the `bin` folder.
Click it, it will run! Now you may delete `x3dview.bat` and then rename `x3dview1.bat` back to `x3dview.bat`, it will still work!

Now you have to decide where you want to keep this software, for example, in your home directory (your user's directory).
If you are ok with having this software in the `Downloads` folder, skip this step.
Drag the `x3dview` directory (the one that contains the `bin` and `lib` folders) to your directory of choice.

Now, navigate to the `bin` subfolder, create a shortcut for x3dview.bat, and move this shortcut to your desktop. Click the shortcut, the X3D Viewer will run!

You may prefer to change the icon of the shortcut, and/or move the shortcut to the "Start" button, but basically that's all with the installation.

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
