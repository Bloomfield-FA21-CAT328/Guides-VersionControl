# Building and Releases

Here's a guide for building executables in Unity.  

## Building in Unity
If your project is using Unity, here are the formats that should be added to a release:

1. Linux 
2. Mac 
3. Windows 32bit 
4. Windows 64bit

### Create "Builds" folder
Before starting, make a folder named _Build_ or _Builds_. The latest GitHub default .gitignore includes both of these folders. If you initialized your project's .gitignore from GitHub, these files will be ignored, which is what you want. You do not want to check in a _Build_ or _Builds_ folder, you are supposed to create a Release in GitHub and attach it to that!

### No development builds!
Also, make sure "Development Build" is **unchecked** for the "release", especially when exporting to Mac, otherwise, you will have to read http://superuser.com/questions/478768/running-app-on-macosx-mountain-lion-job-failed-to-exec3-for-weird-reason-13 and use a Mac to do chmod u+x <Application.app>/Contents/MacOS/<application binary> to produce a working version!

### Build guide
Here are the steps in **File -> Build Settings** to do each version:

#### Linux

1. Select Target Platform - Linux
2. Select Architecture - x64 + x86_64 (Universal)
3. Click **Build**
4. In your project's folder, **use the folder named Build or Builds**, and then create a folder named _ProjectName_\-Linux
5. Name the executable the name of your project. _NOTE:_ Eventhough it defaults the name to .x86, it will create an executable for bot x86 and x86_64. 
6. Wait.
7. Zip up the folder _ProjectName_\-Linux


#### Mac OS

1. Select Target Platform - Mac OS X
2. Select Architecture - x86_64
3. Click **Build**
4. In your project's folder, **use the folder named Build or Builds**, and then create a folder named _ProjectName_\-Mac
5. Name the executable the name of your project.
6. Wait.
7. Zip up the folder _ProjectName_\-Mac

_NOTE: This configuration will work on most Macs since 2006 and will run on Mac 10.6+_

#### Windows

1. Select Target Platform - Windows
2. Select Architecture - x86
3. Click **Build**
4. In your project's folder, **use the folder named Build or Builds**, and then create a folder named _ProjectName_\-Win_x86
5. Name the executable the name of your project.
6. Wait.
7. Zip up the folder _ProjectName_\-Win_x86
8. Select Target Platform - Windows
9. Select Architecture - x86_64
10. Click **Build**
11. In your project's folder, **use the folder named Build or Builds**, and then create a folder named _ProjectName_\-Win_x86_64
12. Name the executable the name of your project.
13. Wait.
14. Zip up the folder _ProjectName_\-Win_x86-64

#### Files made
When done, you should have a bunch of zip files, and folders like so:

![](Filelist.png)

## Release
Follow the instructions for [Creating Releases](https://help.github.com/articles/creating-releases/), and upload your zip files for your project.

For the Intro to Game Programming class, you should use the version number V1.0.0 for the initial build. If you make changes to the project after, you should also do a new build and bump the version number to V1.0.1 if it's a minor bug fix, V1.1.0 if it is adding new features of functionallity. If it's a complete rewrite, then you can do V2.0.0.

