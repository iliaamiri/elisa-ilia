---
layout: default
title: Batch File Creation
nav_order: 4
---

# **How to Create a Batch file?**
{: .no_toc }

In this section, you will learn: 

* basic batch file commands
* using navigation commands
* creating a batch file

{: .fs-6 .fw-300 }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What is a Batch File?

A batch file is a script file that contains commands that are to be executed in a orderly manner. The significance of batch files is the convenience of executing commands automatically in a terminal without needing to re-type. 

---

## Common Batch File Commands

Let's learn commands! Here are all the commands that you may be using in your batch file:

* **title**: provides a title for your batch script in CMD window. 
* **cls**: clears command prompts. 
* **rem**: short for **remark**, is a comment command that will not be used for scripting.
* **(" .\ ")**: directs to root folder.
* **pause**: breaks the automatic scripting in batch file. Will need user to "Press any key to continue.." to resume. 
* **start""[website]**: launches browser with desired website. 
* **echo**: terminal will repeat text back.

---
## How to Create a Batch File?
In this section, you will be following along the instructions to creating your first batch file!

### Step 1 - Create a New Text Document in Desired Location

For starters, it is easier to create a text file right from the desktop. 

First, press `Win + D` to display your desktop. Then right-click your desktop. There should be a drop-down menu, where you can press `New`. Press the option `Text Document` to create a new text file onto your desktop. 

![Creating a new text file](https://i.imgur.com/Jeydx0n.jpg)

 Now you can name the file whatever you like!

![Text file created and is ready to get a new name](https://i.imgur.com/iWYxMnL.jpg)

##### After renaming: 
![Text file created and renamed GUI](https://i.imgur.com/ViZxvCu.jpg)




### Step 2 - Start Typing Commands into Text Document

First, double-click on the new file and start the text file with `@echo off`. It should be the first line of the file. 

**Note**: having `@echo off` will ensure that batch file does reveal all the command prompts. 

![Opening the text file and starting to write batch commands](https://i.imgur.com/20scGST.jpg)


---
#### Let's use the common batch commands you learned!

Remove your first line of text by pressing `ctrl + A` then `ctrl + X`. Copy and paste the code provided below into the text file you just created. 


```cmd
@echo 

title this is an example! 

rem look at the terminal title. It has changed! Now I will pause this. 

pause

cls

pause

start "" https://iliaamiri.github.io/elisa-ilia/

echo that popped up the website! 

pause
```

**Note**: notice how the `@echo` does not have `off` beside it? 

---
#### Change the file from text to a batch file

Head to `File` in the top bar, `Save` then press `Save As`. 

![save as](https://i.imgur.com/97GWVaf.jpg)


This allows you to rename your file. **Make** sure to end your file name with `.bat`. Ending it with `.bat` will automatically change it into a batch file. After, press `Save` when you're done renaming. There should be a new batch file made in desktop. 

**Note**: file will **not** be a batch file if it does not end in `.bat`.

![](https://i.imgur.com/8pbvzRg.jpg)





## Results
Now you get to see your first batch file scripting! Head to the desktop with `Win + D`.


Double-click on the new created batch file. 

![end with bat](https://i.imgur.com/GUFM8Fr.jpg)

Here is what you're supposed to see in your terminal:

![batch 1](https://i.imgur.com/3TdEi7t.jpg)


![batch 2](https://i.imgur.com/IMEy6rb.jpg)


**Note**: Notice that the terminal looks messy. However, `cls` cleared some of the command prompts. Not only that, it is messy because we didn't have `@echo off`. In addition, `rem` command is displayed in the terminal when it's not supposed to. Next steps will show you the difference of `@echo` and `@echo off`. 


### Change back to @echo off

In order to edit batch file, you need to use Notepad again. 


Right-click the batch file from desktop and press `edit`. It will automatically open Notepad. 

![edit](https://i.imgur.com/3O9KhGn.jpg)


Add `off` beside to `@echo` to get `@echo off`. Go back to `File` and `Save`. 

![echo off](https://i.imgur.com/cbFqpM8.jpg)

Run the same batch file and notice the differences:

![new batch 1](https://i.imgur.com/Y7NRwOh.jpg)


![new batch 2](https://i.imgur.com/MRSG2GO.jpg)




See how much cleaner the terminal is? With `@echo off`, it does not show any of the command prompts unless indicate with the command `echo`. 

Congratulations for creating your first batch file!
