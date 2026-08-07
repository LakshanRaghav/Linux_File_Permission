# Linux_File_Permission
As part of Google certified cybersecurity certification this is an activity to assess permissions of files and directories for the appropriate owners in Linux filesystem 

# File permissions in Linux

## Project description

In Linux the FHS (Filesystem Hierarchy Standard) Uses custom permission to all the type of the user needs access to different files to different privileges. There are commands in Linux to set and maintain these access privileges. This project will clarify how to set permission appropriately for the users to the corresponding files of different types.

## Check file and directory details

![](https://raw.githubusercontent.com/LakshanRaghav/Linux_File_Permission/refs/heads/main/supporting_documents/Screenshot_8-8-2026_23527_fz3oj5puswpnqf6l5m4syc5eg5cm5mfqei3yxi2ccl2bfpzszbaa.us-west1-c.resources.bumper-boa.jpeg)  
The directory contains a lot of files and a directory.   
**ls** is a command used to list out existing directories and files in the working directory.  
**ls \-la** is special command used to list all the files including hidden files with their existing permission in the working directory

## Describe the permissions string

From the above we can see a lot of information about the permission for each file and directory.  
To understand the confusing characters, let's take an example from above to discuss its meaning.  
Directory **drafts drwx- \-x- \- \-**   
Since it is a directory the initial char is set to **d…..** ‘  
The owners are divided into three types, A user, A group, Others  
There are three types of permission can be assigned to a directory or file :   
r (read only) , w (write only), x (Execute only)  
Therefore every permission access string consists of 10 chars where the first char defines if it's a file or a directory. The rest into three chars of three parts in an order of the owner's user :  2nd to 4th chars, Group : 5th to 7th chars, Others : 8th to 10th chars correspondingly.  
And the directory drafts allows user to read, write, execute and the users belong to the group to only execute it.

## Change file permissions

![](https://raw.githubusercontent.com/LakshanRaghav/Linux_File_Permission/refs/heads/main/supporting_documents/Screenshot_8-8-2026_32943_docs.google.com.jpeg)  
Here we have executed **chmod o-w project\_k.txt** to remove write permission to others on project\_k.txt file.  
Here in **o-w** , **o** represents the owner type Others and (-) symbol means to remove , (w)the write permission.  
**Chmod** command helps in changing the permission to files and directories to appropriate access to different type of owners. 

## Change file permissions on a hidden file

![](https://raw.githubusercontent.com/LakshanRaghav/Linux_File_Permission/refs/heads/main/supporting_documents/Screenshot_8-8-2026_32956_docs.google.com.jpeg)  
A hidden file is a file whose file name starts with  (.) dot and not visible is list command.  
Here **chmod u=r,g=r .project\_x.txt** gives absolute real only permission to user and group for the hidden file .project\_x.txt . The (=) symbol give only absolute described permission to the owners described.

## Change directory permissions

![](https://raw.githubusercontent.com/LakshanRaghav/Linux_File_Permission/refs/heads/main/supporting_documents/Screenshot_8-8-2026_3308_docs.google.com.jpeg)
Similar to previous actions here we replicate similar commands using **chmod** to change access permission for a directory.  
**chmod g-x drafts/**

## Summary

In Summary this activity explains how to list all the files including hidden files with their access permission to different types of owners. Also how to use chmod efficiently to set and maintain different types of access permission for appropriate owners .

