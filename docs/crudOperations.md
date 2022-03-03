---
layout: default
title: CRUD Operations
nav_order: 3
---

# **CRUD Operations**
{: .no_toc }

As a super user, you might find yourself the need to manage files and folders via CMD. CRUD is an acronym of four things: Create, Read, Update, and Delete.

In this section, we'll go through all CRUD operations on files, and by the end, you'll be able to:
* Create a new folder
* Create a new file
* Read files
* Update the contents of the file
* Delete a file

{: .fs-6 .fw-300 }

---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Reading an Existing File using `type`
To read the contents of an existing file, use this format:
```cmd
C:\Any_Path> type <the path to the existing file>
```

Example:
![Example of reading the content of an existing file using `type`](https://imgur.com/pR2teC8.png)

## Creating a new Folder using `mkdir`
To create a folder using `mkdir`, use this syntax:
```cmd
C:\Any_Path> mkdir <name of the directory>
```

Example:
```cmd
C:\Users\User> mkdir tmp
```

The command above will create a new folder under `C:\Users\User`, which is our user home directory.

![create new folder](https://imgur.com/rD88TgS.png)

**Note:** Most of the command-lines will not show you any output when they do their jobs successfully and without errors. They are silent unless there's a problem!

## Creating a new File using `echo`
To create a file using `echo`, use this syntax:
```cmd
C:\Any_Path> echo <content> > <name of the file[.fileExtension]>
```

Example: 
```cmd
C:\Users\User\tmp> echo The content of the file > New_File.txt
```

The command above will create a text file named "New_File" and fills it with '`The content of the file`' content.

![create new file and filling it with some content](https://imgur.com/uY02BVh.png)

The `>` character means you want to fill the file on the right-side with the contents on the left-side.

### Creating an Empty File using `type`
You can create an empty file use the `type` command like the following:
```cmd
C:\Users\User\tmp> type nul > New_Empty_File.txt
```

The `nul` phrase indicates emptiness.

## Renaming a Folder or File using `ren`
To rename a folder, you can use this syntax:
```cmd
C:\Any_Path> ren <directory_you_want_to_change> <new_directory_name>
```

Example: Let's rename our `folder_1` folder to `folder_1_ranmed`.
```cmd
C:\Users\User\tmp> ren folder_1 folder_1_renamed
```

![folder renaming](https://imgur.com/31Ffw63.png)

To rename a file, ues the same syntax. But, mention file names instead of folders.

Example: Let's rename our `New_File.txt` to `cmd_is_fun.txt`.
```cmd
C:\Users\User\tmp> ren New_File.txt cmd_is_fun.txt
```
![file renaming](https://imgur.com/Q00kgec.png)

## Updating an Existing File
Unfortunetly, there are no pre-installed text editors for CMD. There used to be one a long time ago that looked like the image below.

![Old edit command](https://www.computerhope.com/jargon/e/doseditwindow.jpg)

**Note:** In the good old days, people used to call Windows' shell "MS-DOS" instead of Command Prompt (CMD).

But, we can still append and update the files using CMD. Doesn't hurt to learn those!

To append data to an existing file, just replace the `>` character with `>>`.

Here's an example:
```cmd
C:\Users\User\tmp> echo New informaiton added to the next line of this file >> New_File.txt
```

![appending to an existing file](https://imgur.com/TSSpmFb.png)

While with `>>` you can append data to a file, using the `>` character will replace the whole content of the existing file with the new content you provide.

For example, the command below will replace *everything* in our "New_File.txt" with '`New content`':
```cmd
C:\Users\User\tmp> echo New content > New_File.txt
```

![replacing the whole content with new content](https://imgur.com/LG9lCFN.png)

## Delete a File using `del`
To delete a file, use this format:
```cmd
C:\Any_Path> del <file name>
```

Example: Let's delete our `cmd_is_fun.txt` file.

**Caution:** Any file deleted using `del` command cannot be recovered. Therefore, use it with extreme caution.

```cmd
C:\Users\User\tmp> del cmd_is_fun.txt
```

![deleting a file](https://imgur.com/dHt3eL4.png)

## Delete a Folder using `rmdir`
To remove a folder, use the following format:
```cmd
C:\Any_Path> rmdir <directory path>
```

Example: Let's remove the empty folder, `folder_1_renamed`.
```cmd
C:\Users\User\tmp> rmdir folder_1_renamed
```
![deleting an empty folder](https://imgur.com/ml1g2b7.png)

As seen above, we successfully deleted this folder. But, what if we ever wanted to remove a folder that contained other sub-folders or files?

Interestingly, `rmdir` alone will not allow us to delete such a folder. To make sure, let's try and delete `C:\Users\User\tmp` folder, in which we are in.

![trying to delete a folder that contains a sub-folder](https://imgur.com/bTKdGOv.png)

As you can see, CMD is not happy with this. It's telling us that "the directory is not empty". 

**Note**: The `tree tmp /f` command is used to clarify that the `tmp` folder contains a sub-folder "folder_2" and a file called "important_information.txt" nested in it.

The philosophy of this is that Windows guesses that there might be important files or sub-folders that you should make sure you want to delete them too. One way to fix this is to manually delete every files and empty sub-folders first, and then run this command again.

However, what if there are so many files and sub-folders *and* you are completely sure you don't need them? Well, you can include the `/s` flag to force the deletion of all the nested sub-folders and files of that folder.

**Caution**: Be advised that once you run `rmdir` on a folder with `/s` flag, it will completely delete not just that folder but *all of its existing nested sub-folders and files*, and this action is not recoverable! Make sure what folder you are deleting, checking all the sub-folders and files using `tree <directory path> /f` command.

**Note**: Running `rmdir` with `/s` flag will ask you to confirm your decision. However, you should still be careful.

Having said all that, let's delete the `tmp` folder forcefully:
![force deleting a directory](https://imgur.com/KFpuRWs.png)

That's so much it!
