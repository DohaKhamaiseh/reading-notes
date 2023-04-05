## The Command Line :

 ### A command line, or terminal, is a text-based interface to the system. we can enter commands by typing them on the keyboard and feedback will be given to us similarly to text.
### the steps  to get one is different according  to the used system, we use Linux so here are the steps :
### 'right-click' on the desktop and choose the option 'Open in terminal'.
### or open the terminal by searching for it in the search box on your computer 

## Basic Navigation : 
### we can move through directories on Linux by using these 3 commands:
### pwd ---> to know where I am
### cd directory name ---> to move to this directory
### if we wrote cd without determining a directory it will go to the home 
### ls --> to know what is inside the current directory 

## More About Files :
### interesting characteristics of files and directories in a Linux environment :
1. Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file.
   
2. Linux is Case Sensitive : as such it is possible to have two or more files and directories with the same name but letters of different case.
   
3. Spaces in names : To get around this we need to identify to the terminal that we wish file name to be seen as a single command line argument. There are two ways to go about this: Quotes : 'file name'    Escape Characters: file\ name
   
4. Hidden Files and Directories : To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.

## Manual Pages : 
### we can make the most of the Linux commands we are learning by always using the manual pages that will remind us of all stuff related to forgotten command, when that happened 

## File Manipulation :
### all commands mentioned in the article are very important and all one should know them, it is very good how we can use the mv command to rename a directory, also I think we need undo command  

## in the End, here is a Cheat Sheet for all above articles : [Cheat Sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)