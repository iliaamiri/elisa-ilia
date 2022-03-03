---
layout: default
title: Troubleshooting
nav_order: 8
---

# Troubleshooting
{: .no_toc }

{: .fs-6 .fw-300 }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Can't delete a file?
In general, there are two cases where you'll encounter to an 'Access Denied' error while trying to delete a file via CMD. Either you don't have access to write or modify that file, or that file is 'Read Only'.

If it's the first case, you can't do so much. However, if the file is in Read Only mode, you may *force* delete the file using the `/f` flag in `del` command.

```cmd
C:\Any_Path> del <file name> /f
```

Here's an example force deleting a Read Only file in practice:
![Force deleting a read only file](https://imgur.com/m7YlRio.png)

## Can't delete a folder that is being used in another process?
In some cases, you might be trying to delete a folder where you either have opened in another terminal, another window, or more interesting, the folder where you are running the command in!

For example, if you try to even force remove a folder with all its sub-folders and files, while doing it in the folder itself or its sub-folders, you will encounter with an error.

![Can't delete a folder when you are in it](https://imgur.com/rGLjjjx.png)

The easiest solution would be to first change your directory to somewhere other than inside the folder you want to delete.

Also, make sure you don't have any other open applications that currently use the directory, or other open terminals or window navigating inside that folder.


## Shutdown command is not working?

You may encounter a problem where your `shutdown -r` is not activating right away. If you re-type the command, it will inform you that it has already been scheduled. 

All you need to do is wait a bit because the command takes less than 60 seconds to activate. 

![Shutdown](https://i.imgur.com/v2mCRSt.jpg)
