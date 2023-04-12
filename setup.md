# Setting Up Your Computer For App Academy  

In order to be successful in the course, your computer needs to be setup in a very specific way. If the setup is correct, you will not waste your time fighting the setup of tools and applications, so you can concentrate on the new material you are learning.

***
***
<br>

# **1.** Installing the basics:

First we need to install a few simple things for all opperating systems.

 - [Google Chrome](https://www.google.com/chrome/)
 - [Visual Studio Code](https://code.visualstudio.com/download)  

***
<br>

# **2.** WSL (for Windows users only):  

## **If you are not using windows, please proceed to step 3.**  
<br>

In the Learning Challenges and Prep Work, you used **Git For Windows** which allowed you to use UNIX-style commands on your Windows machine. This approach allowed you to speed up the setup process and was sufficient for completing the Learning Challenges and Prep Work, but this approach is not sufficient for completing all of the practices and assessments for the course.  

Today we will be switching completely to WSL.

## Installing WSL:  

Future versions of Windows will include an automatic installer for WSL, but for now you will have to use the manual install instructions:  

- [Windows Subsystem for Linux Installation Guide for Windows 10 / 11](https://learn.microsoft.com/en-us/windows/wsl/install)

Follow this guide to install WSL 2 and Ubuntu Linux.    
  
# Tips for using WSL:

You will launch the **Ubuntu terminal** when the instructions in our curriculum tell you to open a Terminal.

**You should always store your code files in your Ubuntu home directory, and not in your Windows users home directory on your C: drive.** Many of the tools we use will perform better and be more stable if the files exist on the Ubuntu filesystem.

If you need to access the files in your Ubuntu home directory from Windows Explorer you can type `Windows + R` to bring up the run command dialog. Then type `\\wsl$\home\<your-user>` replacing `your-user` with your Ubuntu user name (you can find this out by typing `whoami` at your Ubuntu terminal prompt.)

If you want to access your Windows hard drive from Ubuntu you can use the path `/mnt/c` inside of the Ubuntu virtual machine. You should open project files in your Ubuntu files, not from your Windows files. Move project files from your Windows file system to your Ubuntu file system before opening and changing project files.

If you ever need to restart the Ubuntu virtual machine, you need to open a Powershell window and run the following command:

```
wsl --shutdown
```
Next time you open the Ubuntu terminal it will start the virtual machine back up.  

# Installing WSL Visual Studio Code extension:  

> Once you are finished setting up WSL, it is important to also install the extension for Visual Studio Code.  

### **To do so, please complete the following:**  
  - Open Visual Studio Code  
  - Find the Extensions tab on the left or by using the default shortcut (`Ctrl+Shift+X`)  
  - Search for WSL and click on the extension, it will be the one published by Microsoft  
  - Once found just click `install`  
  - Once completed you will now be able to open Visual Studio Code through your Ubuntu terminal using the command: 
  
  >  ```code .```  
  - Make sure to only run this inside your **Ubuntu Terminal**  

### **Git:**  

Git is a Version Control System, or VCS. It keeps track of a set of files over time, and is used through the command line.  
  - Return to your Ubuntu Terminal.
  - You need to configure Git, so type `git config --global user.name "Your Name"`, replacing "Your Name" with your real name.
  - Then type `git config --global user.email your@email.com`, replacing "your@email.com" with your real email.

Check that Git is installed and configured properly by typing the following commands into the Terminal. You should see your real name and real email address returned.  

```
git config --global user.name    # your name returned

git config --global user.email   # your email address returned
```  

***
<br>

# **3.** MacOS Configuration (mac users only):  

## **If you are not using mac, please proceed to step 4.**  
<br>

> *Note: You may have already completed this section during prepwork, if that is the case please proceed to step 4.*
<br>

### **Visual Studio Code:**  

Once you have installed Visual Studio Code please complete the following:  
  - Check that Visual Studio Code is installed and working properly by finding it in your Applications directory, and double-clicking to open it.  
  - To open the VS Code editor, open the Command Palette (`Cmd+Shift+P`) and type "shell command".  
  - Click on `Shell Command: Install 'code' command in PATH command`  
    - this will allow you to use the `code` command from the Terminal to open projects in VS Code.  

***
<br>

### **Homebrew:**  

Homebrew is a piece of software for macOS that lets you install extra unix software on your Mac.  
  - Select "Terminal" to start Terminal.
  - Open Safari and navigate to https://brew.sh.
  - Copy the command to be pasted into the Terminal by clicking on the clipboard icon.
  - Paste the command into Terminal and press Enter.
  - Press Enter when prompted.
  - Enter your password when prompted. Wait...this could take a long time!  

  You can check that Homebrew was installed correctly by typing `brew doctor` into the Terminal. If it reads that "Your system is ready to brew.", then you are done. If not, address the errors that you see. 
  
  > *If there are any warnings, you can ignore them for now and continue*.  

***  
<br>

### **Git:**  

Git is a Version Control System, or VCS. It keeps track of a set of files over time, and is used through the command line.  
  - Return to your Terminal.
  - Type `brew install git`.
  - You need to configure Git, so type `git config --global user.name "Your Name"`, replacing "Your Name" with your real name.
  - Then type `git config --global user.email your@email.com`, replacing "your@email.com" with your real email.
  - Finally, install xcode command line tools by typing xcode-select --install.  

Check that Git is installed and configured properly by typing the following commands into the Terminal. You should see your real name and real email address returned.  

```
git config --global user.name    # your name returned

git config --global user.email   # your email address returned
```  

***
<br>

# **4.** Configuring Default Git Branch:

Now, you will complete some further configuration that will help you to start integrating Git with GitHub.

First, enter the following command in your Mac or Windows terminal:

```
git config --global init.defaultBranch main
```

This specifies that your default Git branch should be the `main` branch.

***
<br>

# **5.** Installing NodeJS / Mocha:  

***
<br>

# **6.** Setting up SSH for Github: