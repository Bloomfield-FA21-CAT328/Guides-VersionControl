# Building and Releases

Here's a guide for building executables in Unity. 

## Make a commit to GitHub! 

Before you build, you should make a commit to GitHub. When you make a release, GitHub will also make an archive of the source code, as well as make a "tag" for this particular version. A *tag* is a link in Git that can be referenced to a certain commit. This is useful if you need to compare different versions of builds.

## Building in Unity
Here are the formats that should be added to a Release:

1. Linux 
2. Mac 
3. Windows 32bit 
4. Windows 64bit

* Why make a Linux build? Because Unity can! If you run SteamOS, you could still play your Unity creation! 
* Why make a Mac build? Because Unity can, and I use a Mac at home an work, so if you want me to view your project, you need to make a Mac build. 
* Why make 2 windows build? Because Unity can, and because the computers in the labs would sometimes run into issues with one build or the other. Better safe than sorry!

### Create "Builds" folder
Before starting, make a folder named _Build_ or _Builds_ in your project's directory. The GitHub default *Unity .gitignore* includes both of these folders. So, if you initialized your project's repository *.gitignore* from GitHub, these files will be ignored which is what you want. You do not want to check in a _Build_ or _Builds_ folder, you are supposed to create a Release in GitHub and attach it to that!

### No development builds!
Also, make sure "Development Build" is **unchecked** for the "release", especially when exporting to Mac, otherwise, you will have to read [Running app on MacOSX Mountain Lion: Job failed to exec(3) for weird reason: 13](http://superuser.com/questions/478768/running-app-on-macosx-mountain-lion-job-failed-to-exec3-for-weird-reason-13) and use a Mac to do `chmod u+x <Application.app>/Contents/MacOS/<application binary>` to produce a working version!

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
2. *NOTE: Prior to Unity 2017.3 you would need to select Architecture - x86_64*
3. Click **Build**
4. In your project's folder, **use the folder named Build or Builds**, and then create a folder named _ProjectName_\-Mac
5. Name the executable the name of your project.
6. Wait.
7. Zip up the folder _ProjectName_\-Mac

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

You will just need each of the .zip files to add to your release in GitHub.

## Or just use _Prof Pollati's Unity Utilities - Build Buddy_!

Save your self a lot of hassle. Add [Build Buddy](https://github.com/ProfPollati/ProfPollatiUnityUtilities/releases/latest/download/BuildBuddy.unitypackage) to your project, and you just have to go to the menu and select **Pollati Utilities -> Build Buddy** and then wait for Unity to build all the projects. The plugin will handle all the building, zipping, and naming of everything for you! If you do not have a particular build component installed, Build Buddy will warn you about it, and build what it can.

## Posting a Release

Follow the instructions for [Creating Releases](https://help.github.com/articles/creating-releases/), and upload your zip files you made in the build process for your project. If you drag the zip files, make sure you drag it to where it says *"Attach binaries by dropping them here or selecting them."*, otherwise you will be limitted to uploading only small files.

![](AttachBinaries.png)

### Naming of *Tag Version*
 
For these classes, you should use the version number V1.0.0 for the initial build. If you make changes to the project after, you should also do a new build and bump the version number to V1.0.1 if it's a minor bug fix, V1.1.0 if it is adding new features of functionallity. If it's a complete rewrite, then you would do V2.0.0.

### Naming of *Release Title*

Ideally, you can just say "Initial Release", but I'm sure most of you will get creative here.

### Publish Release

Make sure you click on the **Publish release** button and not the *Save draft* button. It it's not published, then we won't be able to see the files.
