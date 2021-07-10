# Swift ARM Guide Ubuntu Guide Virutal Machine

This guide will help you install and manage Swift (and flavours of Swift) on Swift ARM on a Virtual Machine: Parallels or UTM. Currently, VMWare does not support ARM M1 Macs.

## Ubuntu ARM Instillation 

### Download
Ubuntu ARM is distributed primarily as as server, which means it doesn't have GUI automatically as a part of its package. If you want a GUI (you do) you will need to continue to the next instructions after you have downloaded and installed Ubuntu ARM.
[Download Page](https://ubuntu.com/download/server/arm)

### Install GUI
After you  have installed Ubuntu ARM (Server), you will need to run the following command to install a desktop GUI.

> sudo apt install ubuntu-desktop

Now that you have a GUI, you can login and use the Terminal app.

### Store
If you want the store to be avilable, you can run this installer as well. It is not necessary.

> sudo apt install gnome-software

### Visual Studio ARM Instillation
If you want to install Visual Studio, you will need to go to this page [here](https://code.visualstudio.com/download) and choose the .deb ARM version of the software. Then use one of following commands to install in the Terminal.

#### Method 1
> sudo apt install /path/to/visualstudio.deb

#### Method 2
> sudo dpkg -i /path/to/visualstudio.deb

**TIP:** Typing the path to a file takes a lot of work. In either of the methods above, you can simply type `sudo apt install` and then drag the .deb file on top of the Terminal. 

## Swift ARM
There are two ways to install Swift ARM. One is by installing it on your Ubuntu System in such a way that it integrates it into the system. Another is by downloaing and running it within a package. I prefer the second method, becuase it doesn't put Swift binaries in the standard directories and allows me to delete the toolchain entirely if I want to replace it with a new version or run an experimental version.

1. Open FireFox on your Ubuntu ARM Virtual Machine.
2. Go to https://github.com/futurejones/swift-arm64/releases
3. Select the latest version (as of writing this, that would be Swift 5.4.1 RELEASE for Linux - AArch64)
3. You will see a list of pre-packaged Swift toolchains for your version of Ubuntu (If you installed version 20.04, then you will choose that version. You will also notice that there are several files that referene your Linux distribution; you will download the .tar.gz not the one that ends in .sig. It should be a file about 450MB+.
4. Click the link and select Save File. This should download a copy into your Downloads folder. 
5. Now right click and press "Extract Here"
6. This will create a file with a long, complicated name such as `swiftlang-5.4.1-ubuntu-20.04-release-aarch64-15-2021-05-27`. Don't be overwhelmed by the long name as the name just tells you a lot about the build and binaries within. 

## Test Swift on ARM
1. Open the folder that was created in the section 'Swift ARM'. 
2. Navigate to usr/bin/swift
3. Open the Terminal app. 
4. Drag the swift binary (within the bin folder) over the terminal screen. 
5. Press enter. This should run the siwft repl. You can now type some code like ```let x = 100```
