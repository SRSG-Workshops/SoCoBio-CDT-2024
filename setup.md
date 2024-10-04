---
title: Setup for SoCoBio Computational Research Skills
---


# Best Practices in Data Organisation Using Spreadsheets

## Data for Spreadsheets Lesson

The data used in this lesson comes from a project observing a small mammal community in southern
Arizona, US. This is part of a project studying the effects of rodents and ants on the plant
community that has been running for almost 40 years. The rodents are sampled on a series of 24 plots,
with different experimental manipulations controlling which rodents are allowed to access which plots.
This is a real dataset that has been used in over 100 publications. It is published at [Ecological Archives](http://esapubs.org/archive/ecol/E090/118/) and can be found on [Portal Project Database](https://github.com/weecology/PortalData). This data is open and free to use for research purposes.

For the purposes of training, this data has been simplified a bit (you can still download the full dataset and work with it using exactly the same tools we will learn here). This simplified version of data is available from the [Portal Project Teaching Dataset](http://figshare.com/articles/Portal_Project_Teaching_Database/1314459). In this lesson, you will need to download the following five files from the [Portal Project Teaching Dataset](http://figshare.com/articles/Portal_Project_Teaching_Database/1314459):
-  [messy_survey_data.xls](data/messy_survey_data.xlsx) - this is the main file we will work with. It includes messy survey data
(in Excel's `.xlsx` format) that you will clean during the lesson and use to learn some best practices in
data organisation.


## Install Microsoft Excel

Microsoft Excel is commonly provided by most institutions with the Microsoft Office suite via an instututional licence. 
On Windows and MacOS, Microsoft Excel can be downloaded using the Microsoft Store and the App Store respectively. 
On Linux, you may use Microsoft Excel in a web browser. This is not reccomended and we suggest you use an alterntive such as LibreOffice
instead. If you do not have access to a Microsoft Office licence, please use an alternative such as LibreOffice.


## Install LibreOffice 

In the lesson, Microsoft Excel is used as the spreadsheet software of choice. An alternative spreadsheet software to Microsoft Excel
is LibreOffice Calc. There will be some commands and formatting options which differ between Calc and Excel, but the general workflow 
and ideas for thinking about data organisation in spreadsheets are the same.

### Windows

- Download the Installer
  - Install LibreOffice by going to [the installation page](https://www.libreoffice.org/download/libreoffice-fresh/). The version for Windows should automatically be selected. Click Download Version X.X.X (whichever is the most recent version). You will go to a page that asks about a donation, but you do not need to make one. Your download should begin automatically.
- Once the installer is downloaded, double click on it and an installer for LibreOffice will launch. The default options are fine.

### MacOS

- Download the Installer
  - Install LibreOffice by going to [the installation page](https://www.libreoffice.org/download/libreoffice-fresh/). The version for MacOS should automatically be selected, however you may need to switch to the Apple Silicon version. Click Download Version X.X.X (whichever is the most recent version). You will go to a page that asks about a donation, but you do not need to make one. Your download should begin automatically.
- Once the installer is downloaded, double click on it and drag LibreOffice.app into the Applications folder.

### Linux

- Download the Installer
  - Install LibreOffice by going to [the installation page](https://www.libreoffice.org/download/libreoffice-fresh/). The version for Linux should automatically be selected. Click Download Version X.X.X (whichever is the most recent version). You will go to a page that asks about a donation, but you do not need to make one. Your download should begin automatically.
- Install LibreOffice using the file you downloaded.


# Data Cleaning with OpenRefine

## Introduction to the Data for this Lesson ##
The data used in this lesson comes from a project observing a small mammal community in southern
Arizona, US. This is part of a project studying the effects of rodents and ants on the plant
community that has been running for almost 40 years. The rodents are sampled on a series of 24 plots,
with different experimental manipulations controlling which rodents are allowed to access which plots.
This is a real dataset that has been used in over 100 publications. It is published at [Ecological Archives](http://esapubs.org/archive/ecol/E090/118/) and can be found on [Portal Project Database](https://github.com/weecology/PortalData). This data is open and free to use for research purposes.


## Download Data for OpenRefine Lesson ##

The Portal Project Teaching Dataset is a real dataset that has been used in over 100 publications. We have simplified it
for the purposes of this lesson, but you can download the full dataset (see below for details) and work with it
using exactly the same tools we will learn here.

For this lesson, you will need to download the following file (remember where you downloaded the file!):
*  [portal_project_rodents.csv](data/portal_project_rodents.csv)

Data in some of the columns of the above file (e.g. `geolocation`, `locality`, `county`, `country`, `JSON`) are contrived for the purpose of the lessons and are in no way related to the original dataset.

## Install OpenRefine ##

For this lesson you will need [OpenRefine](http://openrefine.org/) (formerly GoogleRefine) and a web browser.
Download the most recent version of [OpenRefine](http://openrefine.org/download.html) for your operating system,
then follow the instructions below.

[OpenRefine](http://openrefine.org/) is a Java program that runs locally on your machine (i.e. you are not accessing a remote service on the Internet). 
OpenRefine for Mac come with embedded Java, on Windows please select Windows kit with embedded Java, on Linux you will need to install Java separately.

Once it is running on your machine, you access it via your browser at the address [http://localhost:3333](http://localhost:3333). No Internet connection is needed for this as the programme is running locally.

### Windows
- If you have Internet Explorer (or Edge) set as your default web browser, check that you have Firefox or Chrome installed and set either of them as your default browser. OpenRefine runs in your default browser, but may not run correctly in Internet Explorer. You can check how to set your browser as default for [Google Chrome](https://support.google.com/chrome/answer/95417?co=GENIE.Platform%3DDesktop&hl=en-GB) or [Firefox](https://support.mozilla.org/en-US/kb/make-firefox-your-default-browser).
- Unzip the downloaded file into a directory by right-clicking and selecting `Extract...`. Name that directory something like OpenRefine.
- Locate `openrefine.exe` in the extracted folder and launch OpenRefine by double-clicking on it. This will launch a command prompt window first.
- Wait for OpenRefine to launch in your default Web browser, which is where you will interact with the program. If this does not happen, head to [http://localhost:3333](http://localhost:3333) in your Web browser of choice.

### Mac

- Check that you have Firefox or Chrome browser installed and set as your default browser. You can check how to set your browser as default for [Google Chrome](https://support.google.com/chrome/answer/95417?co=GENIE.Platform%3DDesktop&hl=en-GB) or [Firefox](https://support.mozilla.org/en-US/kb/make-firefox-your-default-browser).
- Locate the downloaded `.dmg` file and Ctrl-click it. You may get the warning "macOS cannot verify the developer of “OpenRefine.app”. Are you sure you want to open it?" Click 'Yes'/'Open' to this.
- Drag `OpenRefine.app` into your Applications folder, and Ctrl-click to open it. You may get the warning "macOS cannot verify the developer of “OpenRefine.app”. Are you sure you want to open it?" Click 'Yes'/'Open' to this.
- Wait for OpenRefine to launch in your default Web browser, which is where you will interact with the program. If this does not happen, head to [http://localhost:3333](http://localhost:3333) in your Web browser of choice.

### Linux

- This requires Java to be installed on your computer. If you do not already have it, download [OpenJDK Java](https://openjdk.java.net/).
- Check that you have Firefox or Chrome browser installed and set as your default browser. You can check how to set your browser as default for [Google Chrome](https://support.google.com/chrome/answer/95417?co=GENIE.Platform%3DDesktop&hl=en-GB) or [Firefox](https://support.mozilla.org/en-US/kb/make-firefox-your-default-browser).
- Unzip the downloaded file into a directory. Go to this directory from terminal and type ./refine to start.
- Wait for OpenRefine to launch in your default Web browser, which is where you will interact with the program. If this does not happen, head to [http://localhost:3333](http://localhost:3333) in your Web browser of choice.

## Text Editor ##

A text editor is the piece of software you use to view and write code. If you
have a preferred text editor, please use it. Suggestions for text editors are,
Notepad++ (Windows), TextEdit (macOS), Gedit (GNU/Linux), GNU Nano, Vim.
Alternatively, there are IDE's (integrated developer environments) that have
more features specifically for coding such as VS Code; there are also IDEs
specific to languages will be listed in the appropriate section(s) below.

# The Bash Shell

## Open a Terminal ##

For this lesson, first you need to be able to open a terminal:

- **On Windows:** We'll be using Git Bash. If you've already installed Git Bash then go to the next section. Otherwise, go to [git for windows](https://gitforwindows.org/) and click **Download**, then install it. 
Most of the options can be left on default, but be sure you check these:
  - **Choosing the default editor used by Git:** Make sure **Nano** is selected from the drop-down. If you're comfortable with other editors, feel free to change it, but we recommend Nano - we use it as it's present on Windows, Mac *and* Linux. If you change it, you might not quite match what we're doing on-screen.
  - **Adjusting your PATH environment:** Make sure **Git from the command line and also from 3rd-party software** is selected.
  - **Choosing HTTPS transport backend:** Make sure **Use the native Windows Secure Channel Library** is selected.
  - **Configuring the terminal emulator to use with Git Bash:** Make sure **Use Windows' default console window** is selected.

- **On Mac OS X:** accessed by opening the “Terminal” application, which can be found in the “Utilities” folder which is in your “Applications” folder.
- **On Linux:** this will depend on the Linux distribution you are running, but you should be able to find a "Terminal" application in your desktop's application menu.



## Git Setup ##

### Windows
We'll be using Git Bash for both git and a shell to run it in. If you've already installed Git Bash then go to the next section. Otherwise, go to [git for windows](https://gitforwindows.org/) and click **Download**, then install it.
Most of the options can be left on default, but be sure you check these:
  - **Choosing the default editor used by Git:** Make sure **Nano** is selected from the drop-down. If you're comfortable with other editors, feel free to change it, but we recommend Nano - we use it as it's present on Windows, Mac *and* Linux. If you change it, you might not quite match what we're doing on-screen.
  - **Adjusting your PATH environment:** Make sure **Git from the command line and also from 3rd-party software** is selected.
  - **Choosing HTTPS transport backend:** Make sure **Use the native Windows Secure Channel Library** is selected.
  - **Configuring the terminal emulator to use with Git Bash:** Make sure **Use Windows' default console window** is selected.

#### Mac OS
To use Git you must install the Apple Command Line Tools, this may take a few minutes.  

You can obtain these [from Apple](https://developer.apple.com/download/more/?name=command%20line%20tools%20for%20xcode%2012) (requires your Apple ID)

- Select **Command Line Tools for Xcode 12 (or higher)** and click the link to download the dmg archive.
- If prompted, choose to allow downloads from developer.apple.com
- Open the downloaded dmg archive from the Downloads folder
- Double-click the Command Line Tools.pkg icon to install

Alternatively, you can install the tools from the command line:

~~~
$ xcode-select --install
~~~
{: .language-bash}

#### Linux
Git comes pre-installed on most Linux distributions. You can test if it's installed by running `git --version`. 
If it's not installed, you can install it by running `sudo apt-get install git` or `sudo yum install git`, depending on 
your distribution.


## GitHub ##
We'll be using the website [GitHub](https://github.com/) to host, back up, and distribute our code. You'll need to [create an account there](https://github.com/signup). As your GitHub username will appear in the URLs of your projects there, it's best to use a short, clear version of your name if you can.


## Download Data for Shell Lesson ##

Open a terminal and type the following into the prompt that appears (pressing enter/return after each line):

~~~
$ cd
$ git clone https://github.com/Southampton-RSG-Training/shell-novice.git
~~~
{: .language-bash}

`cd` will move to your home directory, and `git clone` will download a copy of the materials.

This should download all the content for the lesson to a new directory.
Please let the instructors know if you run into any problems.

{% include links.md %}

# Version Control with Git

# Introductory Data Management with R

## Install R and RStudio ##

R is a programming language and software environment for statistical computing and graphics. The RStudio Integrated Development Environment (IDE) is a set of tools designed to help you be more productive with R.

We need to install R and RStudio: 
The latest links can be found on the [RStudio downloads page](https://www.rstudio.com/products/rstudio/download/#download).  Alternatively, you can install R and RStudio from Software Centre if you are using a University of Southampton laptop.

### R

R can be found at [https://cran.rstudio.com/](https://cran.rstudio.com/), from here pick your OS and download the latest release, see below for direct links to your OS.

#### Windows
- [https://cran.rstudio.com/bin/windows/base/](https://cran.rstudio.com/bin/windows/base/)

#### Mac OS
- If prompted, choose to allow downloads from cran.rstudio.com.

- [https://cran.rstudio.com/bin/macosx/](https://cran.rstudio.com/bin/macosx/)
  - For intel based macs choose R-4.*.*.pkg
  - For ARM based macs (M1 etc.) choose R-4.*.*-arm64.pkg

#### Linux
- R is included on many linux distros check to see if it is already present. Else use your package manager (snap, apt, yum), or look [here](https://cran.rstudio.com/bin/linux/)


### RStudio

Your OS should be detected and a link provided under step 2 on this page [RStudio downloads page](https://www.rstudio.com/products/rstudio/download/#download).
Else select your OS from the list under All Installers.

#### Windows

Download and run the .exe file and follow instructions given by your OS.

#### Mac OS

Download the .dmg file.
- If prompted, choose to allow downloads from rstudio.com.
- Open the downloaded dmg archive from the Downloads folder.
- Drag the RStudio icon to the Applications folder to install.

#### Linux
Download the appropriate install file (.rpm or .deb) for your distro.