---
layout: default
title: User Management
nav_order: 5
---

# **User Management**
{: .no_toc }

For a system administrator, having a good foundation of user management on the Operation System is important.

In every Operation System you can create users, manage their privileges, or remove them. Windows handles user authorization pretty advanced. However, this guide doesn't have a focus on advanced Windows System Administration, and does not go through all the details.

In this section, you'll learn how to:
* Create a new User via CMD
* Power a particular User
* Limit a User
* Remove a User

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: To perform any of the tasks above, you'll need to run CMD as Administrator. 

{: .fs-6 .fw-300 }

---

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## User Creation Through Terminal
Although you can create a user using Window's control panel, it is easier to create a user through the terminal. Below will be instructions showing how to create new users. 


### Step 1 - Open Command Prompt
Refer to [opening CMD](https://iliaamiri.github.io/elisa-ilia/docs/navigateThroughFilesystem/#searching-and-opening-cmd-using-windows-search)
 for instructions on how to open command prompt as Administrator. 

![CMD opened as Administrator](https://imgur.com/jTz7xym.png)

![Note icon](https://imgur.com/rDBhoIa.png){: style="float: left" }
>> **Note**: You'll see that the CMD opens on `C:\Windows\system32`. As mentioned in previous sections, this is the default directory path when CMD runs as Administrator.

### Step 2 - Create a Local User

The command line to create a user is in the following syntax:
```cmd
C:\Windows\system32> net user /add <username> <password>
```

Example: Let's make a new User and call it example. Our user will use "badpassword123" as their password.

![New user created](https://i.imgur.com/DJHrzdi.jpg)

#### Create your User in a more Secure Way
Writing the password of your new User in one line is not very secure. A better alternative is to enter their password in a hidden prompt input.

Example: Let's make another new User and call it Mark. Mark asked us to avoid typing his password directly in the one-linear `net` command!

![New user created in a more secure way](https://i.imgur.com/V1FUigJ.png)

Notice that instead of typing the password, we replaced it with an asterisk (`*`), which tells `net` command that we want to enter our password in a secure prompt.

Now, only the creator of the User knows what's the password for Mark!

### Step 3 - [Optional] Make a Local User into an Admin

You can change an existing user into an admin by entering the following syntax:

```cmd
C:\Windows\system32> net localgroup administrators <username> /add
```

Example: We will be using the following new User to change into an admin. 

![Admin user](https://i.imgur.com/u6Ixx51.jpg)

Also, you can use the ** account.

![Warning icon](https://imgur.com/4lS7y5J.png){: style="float: left" }
>> **Warning**: A Windows built-in Administrator can control *everything*! It's similar to the term "sudoer" in Linux, so be careful with whom you are giving this perk to.

To make your User a built-in Administrator, use the following command:
```cmd
C:\Windows\system32> net <username> administrator /active:yes
```

To take this privilege from your User, change the value of `/active` flag to "no".
```cmd
C:\Windows\system32> net <username> administrator /active:no
```

You now know how to create a user, head to [shutdown & restart](https://) and reboot to log into your new account. 
