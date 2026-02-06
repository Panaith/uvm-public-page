# Welcome to Utility Version Manager (uvm)

## Description
This is a simple project to help developers manage versioning for as many Utilities as they need:
- Add/Remove Utilities (Languages, Frameworks, ...)
- Manage multiple versions for each utility  

Currently project is for **Windows** users only.

## Downloads

| Version         | Download                                                                 |
| :-------------- | :----------------------------------------------------------------------- |
| all versions    | [all releases (zip)](https://github.com/Panaith/uvm.github.io/releases)  |

## Commands
Once the uvm project is installed, open terminal (cmd, powershell) and execute any of the following commands:

| Command               | Documentation                                            | What it does                                                                      |
| :-------------------- | :------------------------------------------------------- | :-------------------------------------------------------------------------------- |
| uvm install           | [Installation](#installation-uvm-install)                | install uvm project or refresh already installed uvm project                      |
| uvm config            | [Configuration](#configuration-uvm-config)               | add / remove utilitites to uvm                                                    |
| uvm use               | [Usage](#usage-uvm-use)                                  | select version for your utilities                                                 |
| uvm fix               | [Fix](#fix-uvm-fix)                                      | if something is not working properly, this command will refresh the whole project |
| uvm version           | [Version](#version-uvm-version)                          | retrieve current uvm version                                                      |


## Installation (uvm install)
This process creates installation folder for uvm project.
1. Download latest [release](https://github.com/Panaith/uvm.github.io/releases/latest).
1. Extract .zip file.
1. Open extracted folder find "uvm_install.bat" file and execute it.
1. Click "Yes" in Powershell prompt:  
   ![powershell admin mode](./readmePics/powershell_admin_mode.png)
1. Follow instructions...

### What happens
1. Creates the installation directory "C:uvm".
1. Adds your first utility, that is uvm project itshelf at directory "C:\uvm\uvm".
1. Updates windows environment variables according to added utilities.
1. Continues to Configuration process...

## Configuration (uvm config)
This process allows user to configure uvm project according to his needs.
1. Click "Yes" in Powershell prompt.
1. Follow instructions...
1. Add as many utilities (Git, Java, Gradle, Maven, Node, Flutter, ...) as you need.
1. Remove any utilities that you don't need anymore.

### What happens
1. For example if you add "Java" utility:
    1. Adds "Java" utility directory "C:\uvm\java".
    1. Updates windows environment variables according to added utilities.
1. For example if you remove "Java" utility:
    1. Deletes "Java" utility directory "C:\uvm\java".
    1. Updates windows environment variables according to removed utilities.

## Add multiple versions for each registered utility (manually)
In this process the user manually adds the versions he wants for each of the utilities added in previous step.
For example if you added "Java" utility
1. Go to directory "C:\uvm". Here you will find a subfolder for your utility (i.e if your utility is JAVA: you will find a subfolder named "java").
1. Download as many versions of your utility as you want (i.e if your utility is JAVA: jdk_1.8, jdk_18, ...):
    1. Work with **binary** versions:
        1. Download **binary** version.
        1. Make sure that the downloaded folder is renamed according to its version.
        1. Move renamed folder to the corresponding utility subfolder under "C:\uvm" directory.
    1. Work with executable versions:
        1. Download **executable** version.
        1. Go to "C:\uvm" directory and open the subfolder that corresponds to your utility.
        1. Create a subfolder named according to the version you downloaded.
        1. Execute the executable and select as installation path the subfolder you created in previous step.
1. Do this whenever you want to support a **new** utility version.
1. Keep a structure as:  
   ![utilities - Version - Directory](./readmePics/utilities_versions_directory.png)

### What happens
Now for each utility, you have multiple versions.

## Usage (uvm use)
This process allows user to select which utility and which version he wants to use.
1. Follow instructions...

### What happens
1. Automatically Update windows environment variables according to selected versions.
1. Now you can use the version you selected through terminal (cmd, powershell).

## Fix (uvm fix)
This process will refresh the whole uvm project installation, so you can use use it in case something is not working properly.

## Version (uvm version)
This process will return the current installed uvm project version.

## Future Work
- Support for other platforms (Linux, iOS, ...)
- Add uninstall feature.
- Support basic Utilities: Support for some basic utilities (Git, Java, Gradle, Maven, Flutter, ...) so that user does not need to give details for these utilities when adding one of them.
- Automate "Add multiple versions for each registered utility": Show all available/official versions for all supported utilities and ability to download selected versions from whithin uvm project.

## Most Important
This project was created for my convenience at my free time.  
Testing was time limited, but i don't think you will have any issues hopefully :).  
If you find a bug execute command ["uvm fix"](#fix-uvm-fix) and please [contact me](mailto:psarrid@gmail.com).  
If you want to participate in the project, you are most welcome, [contact me](mailto:psarrid@gmail.com).  
