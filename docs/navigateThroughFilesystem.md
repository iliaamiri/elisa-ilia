---
layout: default
title: Navigate through Filesystem
nav_order: 2
---

# **Navigate through Filesystem**
{: .no_toc }

Any operation system needs the ability to navigate through the filesystem. Windows is not an exception either. There are two most crucial commands that you'll learn how to use:
1. `dir`
2. `cd`

But before that, let's see how to open the Command Prompt on any Windows machine.

{: .fs-6 .fw-300 }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Searching and Opening CMD using Windows Search

### Step 1 - Open up the Windows Search
First, use the `Win + Q` hot key to open up Windows Search.
![Win+Q](https://i.imgur.com/VFqJLEX.png)

You should see a small menu, which is called "Windows Search", usually at the bottom left of your screen.

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: Depending on your task bar position, the Windows Search might appear in other corners of your screen.
<br>

![Windows Search](https://i.imgur.com/l5W6r8F.png)

### Step 2 - Type the word 'cmd' in the Search and Open the Command Prompt.

Now, search for `Command Prompt`, or `CMD`, and click on it to open up the Command Prompt app, aka. (CMD).

![Looking up CMD and clicking on it](https://i.imgur.com/UpcXzv1.png)


### Result
You will see a new window that opens and has a black background.

![CMD Opened](https://i.imgur.com/CmurVWJ.png)

*Welcome to CMD!*

## Running CMD as Administrator
To run the CMD as Administrator there's a small action you need to take when you are opening CMD as mentioned in the *Searching and Opening CMD using Windows Search* section.

<p style="font-size:17px!imortant;"><b>Don't open CMD right-away</b></p>
Before clicking on the Command Prompt application, right click on it, and then choose "Run as Administrator".

![Openning CMd as Administrator](https://imgur.com/Sg70sT4.png)

<p style="font-size:17px!imortant;"><b>Allow CMD to run as Administrator</b></p>
Whenever you want to open an application as Administrator, Windows will confirm with you whether you allow that application to have Administrato level of control on your Operation System or not.

Allow Command Prompt application to run as Administrator by clicking "Yes".

![Allowing CMD to run as Administrator](https://imgur.com/Oz9UDaX.png)

<p style="font-size:17px!imortant;"><b>Result</b></p>
![CMD opened as Administrator](https://imgur.com/jTz7xym.png)

Well-done!

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: By default, when you open CMD as Administrator, the current directory path will be `C:\Windows\system32`. This directory contains the most crucial files of your Operation System that are only accessable to Administrators.
<br>

![Warning icon](https://imgur.com/4lS7y5J.png){: style="float: left" }
>> **Warning**: Be very careful and precise with your actions now! Since you are an Administrator, you can do *everything*, which means you might accidently delete something that you should not, or change settings that can cause undesirable effects on your future experience with Windows.

Before we get started, here's a helpful terminology table that elaborates on the terms we will use later on in this section.

![Helpful Terminologies](https://i.imgur.com/6OS5ozK.png)

Now, let's jump right into the main topic, which is Navigating through Windows Filesystem.


## First Command: `dir`
The `dir` is short for "directory". As the full-name suggests, this command has a very similar funcationality to the `ls -la` command in Linux command-line.

Here's an example of executing the `dir` command in the CMD we just opened:
![Example of executing 'dir' command](https://i.imgur.com/j9jCIjW.png)

The output of this command is a full list of all files and directories available, alphabetically sorted, in the current file path, which in this case is `C:\Users\User` (your User Direcotry).

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: We will go through the Filesystem Hierarchy in Windows and you will be more familiar with the term User Directory later in this guide.
<br>

This output also shows you other details such as:
* The label of the volume of drive
* Volume's Serial Number
* The date and time each were modified
* Total size of all these files amd directories in bytes
* The amount of free space on the disk in bytes
* The total number of files and folders


![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: For more information about `dir` command, read the manual by executing `help dir`, or refer to the Microsoft's Documentation on [Windows Commands Reference - dir](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/dir)


## Second Command: `cd`
The phrase "cd" is an abbreviation for "change directory", which is used to change the current directory to another given directory path. As it is the same for Linux, you can change directories using the signature `cd <the-path-to-another-directory>`.

For example, in the following image, we are changing the directory from `C:\Users\User` to `C:\Users\User\Desktop`.

![Example of changing direcotries using cd](https://i.imgur.com/N7mGcJ5.png)

Now, we are in our Desktop directory, which is an equivalent for `~/Desktop` in a Linux filesystem.

## Windows Directory Structure
Every super user needs to have a fundumental knowledge about the direcotry structure of their Operation System to feel confident with their configuration.

In Windows, the directory separator is `\` instead of `/`, which is the case in Linux. Also, every drive is named by a drive letter, as opposed to linux which is merged to one.

A root folder can be seen as `drive:\` format, which is defined by the name of the drive (partition) on the hard-drive. For instance, the root folder of Windows parition where the OS files are stored, is `C:\`. In Windows, partitions' names start from the letter C and further appear by the next letters (i.e.: C, D, E, F, G, etc.).

Before going through the folders of `C` parition, which is also known as "boot partition", let's change our current directory to `C:\`, and do a `dir` command there.

![cd to C then dir](https://i.imgur.com/lfDFNlU.png)

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: Don't get surprised to see other files and folders in this partition as it is a possibility that some drivers or applications could be stored under the root folder of `C` drive (e.g.: Python, Netcat, etc.).
<br>

The `C` drive may contain these 5 major directories:

### \PerfLogs
PerfLogs folder which is an alternative way of writing "Performance Logs" is usually created by the *Reliability monitor* feature. It stores log files related to the issues and highlites any bad performance on Windows. 

The purpose of these files is to gather all these performance issue logs and send them to Microsoft's Servers, helping them patch those issues and release smoother updates of Windows in the future.

This folder is usually empty, but in some cases, it contains a few kilobytes of performance logs data, which will not take significant amount of disk space.

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: The PerfLogs folder is only accessable to read by Administrator users. To navigate through this folder in CMD, you should first run CMD as Administrator. Refer to our instruction to perform the action said.
<br>

### \Program Files
This folder contains all installed programs (both 64-bits and 32-bits architecture).

On a 64-bits Windows, all the 64-bits programs will be installed in this folder, and any 32-bits or 16-bits programs will be installed in `\Program Files (x86)`.

Here's an example of how a `\Program Files` might look like on a 64-bits Windows.

![Example of how a Program Files directory might look like](https://imgur.com/mqZkDZc.png)

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: You may have noticed the double-quotes in `cd "Program Files"` command. In CMD, it is better to wrap the destination directory between double-quotations whenever there is a space between the name of that directory to avoid mis-understanding for CMD.
<br>

### \Program Files (x86)
This folder only exists on 64-bits editions of Windows. By default, any 32-bits and 16-bits will be installed in this folder though the 16-bits program will not run on a 64-bits Windows.

Here's an example of how a `\Program Files (x86)` might look like on a 64-bits Windows.

![Example of how a Program Files (x86) directory might look like](https://imgur.com/g6TblYJ.png)

### \ProgramData (hidden)
Programs store their public data and access them no matter in which user context they are being running as. For instance, an Antivirus might need to store its latest virus checkers so that every user running that Antivirus can access them.

A program does not have access to store files in this folder, but can create a sub-folder and store their files under it.

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: This folder is hidden. Use the `/a` flag in `dir` to see every hidden folder and links.
<br>

Here's how a `\ProgramData` folder might look like:

![Example of how a ProgramData folder might look like](https://imgur.com/vBTLIeu.png)

### \Users
Very similiar to the `/home` directory in Linux. It contains one folder for every User who has logged in *at least once*.

Also, this folder has two *hidden* sub-folders:
* **Public**: Acts as a shared folder between users' data. Any user who can log in has access to this folder. By default, this folder is shared across the network of authenticated users.
* **Default**: Is a built-in user that was first introduced in Windows 10. Any process that either runs for multiple users or doesn't rely on a user will use this neutral user.

In addition to those, it has two folder-like items called "Default User", which is a link to `C:\Users\Default`, and "All Users", which is a link to the `C:\ProgramData` directory.

Let's see how a `\Users` folder looks like on our terminal:

![Example of how a Users folder might look like](https://imgur.com/wHTCxne.png)

### \Windows
Windows is installed in this folder.

All of the sub-folders store files that form the core features of Windows and [Windows API][Windows API Reference].

Since this user guide's focus is not on this area, we didn't elaborate on the `\Windows` sub-folders in-depth.

However, now you are much more familiar with Windows Directory Structure than most of the daily Windows users world-wide!

Next step would be to [create and manage files and folders][CRUD Operations].

[Windows API Reference]: https://en.wikipedia.org/wiki/Windows_API
[CRUD Operations]: https://iliaamiri.github.io/elisa-ilia/crud-operations
