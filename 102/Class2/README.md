
# Choosing a text editor

Text editor is required for web development. There are variety of text editing software and hard to favor one on the other. 

## **What is a text editor?**

A software which allows you to write and manage text you write to design a website.

### Here are some features you should look for in a text editor:
1. Code completion
2. Emmet (shorthand language)
3. Syntax highlighting
4. Variety of themes
5. Extensions

## Code Completion:
It is a great feature of any text editing software. It allows you to start typing and the code completion feautre will display possible suggestions based on what you originally typed. 
Closing tags is another great option which includes closing tags when you open them, or closing brackets or quotation marks.

## Emmet (shorthand language)
Another nice feature is being able to write HTML and CSS more efficiently. There is a kind of shorthand language called Emmet that can help. Emmet wil speed up your code writing faster than you can imagine. Some text editors come with Emmet built in, or can be added by the means of an extension.

## Syntax Highlighting:
Syntax highlighting makes the text more noticeable by changing it colour. It divides attributes and elements in different colours.

## Varity of Themes:
Some text editors allow web developers to select the background colour of their choice. Usually web developers use dark colored backgrounds and vibrant colored text to make coding more visible.

## Extensions:
Some text editors have great selection of extentions. Extentions are like superpowers wich grow with your need.


Using the software that already comes with your computer

Every computer comes with a text editor like Mac computers come with "Text Edit" and Windows come with "Note Pad".
Usually these text editors do not have formatting options like bold, underline, italic. There are few things need to take care while saving your file, that they should have appropriate extension at the end of the file name. Like HTML file should be called, ".html" or CSS file should be saved with the file format ".css" 

## Third Party Options:

## Notepad++
- A free text editor for Windows computers. 
- It has been in use for many years.
- It has syntax highlighting.
- It also has code, word and function completion.
- It has zoom in and out feature
- It has its own online community and chat room 
- It even has its own searchable wikipage for assistance

## TextWrangler/BB Edit
- It is only for Mac computers which was free to install
- It was retired in 2017
- TextWrangler and Bare Bones softwar has incorporated
- BB Edit need to be purchased
- It comes with a 30 day free trial which can be used as long as required with limited features.
- Full feauters of BB Edit cost $49.99
- It can be downloaded by http://www.barebones.com/products/textwrangler/

## Visual Studio Code
- Visual Studio code is available for Windows, Mac and Linux computers
- It has Emmet shorthand for HTML and CSS.
- It has pretty much everything like:
- Syntax highlighting
- Themes
- Extensions
- Code completion

## Atom:
- free text editor
- for Windows, Linux and Mac
- Brought by GitHub
- Also has:
    - Syntax highlighing,
    - Themes,
    - Extensions

## Brackets:
- free text editor for Mac, Windows and Linux
- Made by Adobe
- It can only supports HTML, CSS and JavaScript
- Live Preview is a strong feature

## Sublime Text:
- Premium software to get im $70
- Fast and responsive
- Syntax highlighting
- Code completion
- Themes and Extensions


## Difference between Text Editors and IDEs

Text editer edits and manages text and manages files. An IDE (Integrated Development Environment)is a suite of different software all coming together. An IDE is a text editor, file manager, a compiler and a debugger all in one software package.
<p>


# The Command Line

Linux has a graphical user interface and it works pretty much like the GUI's on other systems that you are familiar with such as Windows and OSX. This tutorial won't focus on these as I reckon you can probably figure that part out by yourself. This tutorial will focus instead on the command line (also known as a terminal) running Bash.

he command line is an interesting beast, and if you've not used one before, can be a bit daunting. Don't worry, with a bit of practice you'll soon come to see it as your friend. Don't think of it as leaving the GUI behind so much as adding to it. While you can leave the GUI alltogether, most people open up a command line interface just as another window on their desktop (in fact you can have as many open as you like). This is also to our advantage as we can have several command lines open and doing different tasks in each at the same time. We can also easily jump back to the GUI when it suits us. Experiment until you find the setup that suits you best. As an example I will typically have 3 terminals open: 1 in which I do my working, another to bring up ancilliary data and a final one for viewing Manual pages (more on these later).

## So what are they exactly?
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands. Here is an example:

1. user@bash: ls -l /home/ryan
2. total 3
3. drwxr-xr-x 2 ryan users 4096 Mar 23 13:34 bin
4. drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
5. drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
user@bash:

- **Line 1** presents us with a prompt ( user@bash ). After that we entered a command ( ls ). Typically a command is always the first thing you type. After that we have what are referred to as command line arguments ( -l /home/ryan ). Important to note, these are separated by spaces (there must be a space between the command and the first command line argument also). The first command line argument ( -l ) is also referred to as an option. Options are typically used to modify the behaviour of the command. Options are usually listed before other arguments and typically start with a dash ( - ).

- **Lines 2 - 5** are output from running the command. Most commands produce output and it will be listed straight under the issuing of the command. Other commands just perform their task and don't display any information unless there was an error.

- **Line 6** presents us with a prompt again. After the command has run and the terminal is ready for you to enter another command the prompt will be displayed. If no prompt is displayed then the command may still be running (you will learn later how to deal with this).
Your terminal probably won't have line numbers on it. I have just included them here to make it easier to refer to different parts of the material.


# Basic Navigation!

## Introduction:
In this section, we'll learn the basics of moving around the system. Many tasks rely on being able to get to, or reference the correct location in the system. As such, this stuff really forms the foundation of being able to work effectively in Linux. Make sure you understand it well.

So where are we?
The first command we are going to learn is pwd which stands for Print Working Directory. (You'll find that a lot of commands in linux are named as an abbreviation of a word or words describing them. This makes it easier to remember them.) The command does just that. It tells you what your current or present working directory is. Give it a try now.

1. user@bash: pwd
2. /home/ryan
3. user@bash:

A lot of commands on the terminal will rely on you being in the right location. As you're moving around, it can be easy to lose track of where you are at. Make use of this command often so as to remind yourself where you presently are.

## What's in Our Current Location?

It's one thing to know where we are. Next we'll want to know what is there. The command for this task is ls. It's short for list. Let's give it a go.

1. user@bash: ls
2. bin Documents public_html
3. user@bash:

Whereas pwd is just run by itself with no arguments, ls is a little more powerful. We have run it here with no arguments in which case it will just do a plain listing of our current location. We can do more with ls however. Below is an outline of its usage:

ls [options] [location]

In the above example, the square brackets ( [ ] ) mean that those items are optional, we may run the command with or without them. In the terminal below I have run ls in a few different ways to demonstrate.

1. user@bash: ls
2. bin Documents public_html
3. user@bash:
4. user@bash: ls -l
5. total 3
6. drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
7. drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
8. drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
9. user@bash:
10. user@bash: ls /etc
11. a2ps.cfg aliases alsa.d cups fonts my.conf systemd
12. ...
13. user@bash: ls -l /etc
14. total 3
15. -rwxr-xr-x  2 root root 123 Mar 23 13:34 a2ps.cfg
16. -rwxr-xr-x 18 root root 78 Feb 17 09:12 aliases
17. drwxr-xr-x  2 ryan users 4096 May 05 17:25 alsa.d
18. ...
19. user@bash:

Let's break it down:

**Line 1** - We ran ls in it's most basic form. It listed the contents of our current directory.
**Line 4** - We ran ls with a single command line option ( -l ) which indicates we are going to do a long listing. A long listing has the following:
- First character indicates whether it is a normal file ( - ) or directory ( d )
- Next 9 characters are permissions for the file or directory (we'll learn more about them in section 6).
- The next field is the number of blocks (don't worry too much about this).
- The next field is the owner of the file or directory (ryan in this case).
- The next field is the group the file or directory belongs to (users in this case).
- Following this is the file size.
- Next up is the file modification time.
- Finally we have the actual name of the file or directory.
- Line 10 - We ran ls with a command line argument ( /etc ). When we do this it tells ls not to list our current directory but instead to list that directories contents.
- Line 13 - We ran ls with both a command line option and argument. As such it did a long listing of the directory /etc.
- Lines 12 and 18 just indicate that I have cut out some of the commands normal output for brevities sake. When you run the commands you will see a longer listing of files and directories.

## Paths
In the previous commands we started touching on something called a path. I would like to go into more detail on them now as they are important in being proficient with Linux. Whenever we refer to either a file or directory on the command line, we are in fact referring to a path. ie. A path is a means to get to a particular file or directory on the system.

## Absolute and Relative Paths
There are 2 types of paths we can use, absolute and relative. Whenever we refer to a file or directory we are using one of these paths. Whenever we refer to a file or directory, we can, in fact, use either type of path (either way, the system will still be directed to the same location).

To begin with, we have to understand that the file system under linux is a hierarchical structure. At the very top of the structure is what's called the root directory. It is denoted by a single slash ( / ). It has subdirectories, they have subdirectories and so on. Files may reside in any of these directories.

Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )

Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

Here's an example to illustrate:

1. user@bash: pwd
2. /home/ryan
3. user@bash:
4. user@bash: ls Documents
5. file.txt file2.txt file3.txt
6. ....
7. user@bash: ls /home/ryan/Documents
8. file1.txt file2.txt file3.txt
9. ...
10. user@bash:

- **Line 1** - We ran pwd just to verify where we currently are.
- **Line 4** - We ran ls providing it with a relative path. Documents is a directory in our current location. This command could produce different results depending on where we are. If we had another user on the system, bob, and we ran the command when in their home directory then we would list the contents of their Documents directory instead.
- **Line 7** - We ran ls providing it with an absolute path. This command will provide the same output regardless of our current location when we run it.

## More on Paths

You'll find that a lot of stuff in Linux can be achieved in several different ways. Paths are no different. Here are some more building blocks you may use to help build your paths.

- ~ (tilde) - This is a shortcut for your home directory. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents
- . (dot) - This is a reference to your current directory. eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy).
- .. (dotdot)- This is a reference to the parent directory. You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory.
So now you are probably starting to see that we can refer to a location in a variety of different ways. Some of you may be asking the question, which one should I use? The answer is that you can use any method you like to refer to a location. Whenever you refer to a file or directory on the command line you are actually referring to a path and your path can be constructed using any of these elements. The best approach is whichever is the most convenient for you. Here are some examples:

1. user@bash: pwd
2. /home/ryan
3. user@bash:
4. user@bash: ls ~/Documents
5. file1.txt file2.txt file3.txt
6. ...
7. user@bash: ls ./Documents
8. file1.txt file2.txt file3.txt
9. ...
10. user@bash: ls /home/ryan/Documents
11. file1.txt file2.txt file3.txt
12. ...
13. user@bash:
14. user@bash: ls ../../
15. bin boot dev etc home lib var
16. ...
17. user@bash:
18. user@bash: ls /
19. bin boot dev etc home lib var
20. ...

After playing about with these on the command line yourself they will start to make a bit more sense. Make sure you understand how all of these elements of building a path work as you'll use all of them in future sections.

## Let's Move Around a Bit

In order to move around in the system we use a command called cd which stands for change directory. It works as follows:

cd [location]

## Summary

### Stuff we learnt

- pwd
Print Working Directory - ie. Where are we currently.
- ls
List the contents of a directory.
- cd
Change Directories - ie. move to another directory.

### Important Concepts

**Relative path**
A file or directory location relative to where we currently are in the file system.

**Absolute path**
A file or directory location in relation to the root of the file system.

# More About Files

## Everything is a File
Everything under the hood, in Linux is actually a file. A text file is a file, a directory is a file,  your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.

## Linux is an Extensionless System
This one can sometimes be hard to get your head around but as you work through the sections it will start to make more sense. A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is. The following are common extensions:

- file.exe - an executable file, or program.
- file.txt - a plain text file.
- file.png, file.gif, file.jpg - an image.

In other systems such as Windows the extension is important and the system uses it to determine what type of file it is. Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file. As such it can sometimes be hard to know for certain what type of file a particular file is. Luckily there is a command called file which we can use to find this out.

file [path]

Now you may be wondering why I specified the command line argument above as path instead of file. If you remember from the previous section, whenever we specify a file or directory on the command line it is actually a path. Also because directories (as mentioned above) are actually just a special type of file, it would be more accurate to say that a path is a means to get to a particular location in the system and that location is a file.


## Linux is Case Sensitive

This is very important and a common source of problems for people new to Linux. Other systems such as Windows are case insensitive when it comes to referring to files. Linux is not like this. As such it is possible to have two or more files and directories with the same name but letters of different case.

1. user@bash: ls Documents
2. FILE1.txt File1.txt file1.TXT
3. ...
4. user@bash: file Documents/file1.txt
5. Documents/file1.txt: ERROR: cannot open 'file1.txt' (No such file or directory)

Linux sees these all as distinct and separate files.

Also be aware of case sensitivity when dealing with command line options. For instance with the command ls there are two options s and S both of which do different things. A common mistake is to see an option which is upper case but enter it as lower case and wonder why the output doesn't match your expectation.

## Spaces in names

Spaces in file and directory names are perfectly valid but we need to be a little careful with them. As you would remember, a space on the command line is how we seperate items. They are how we know what is the program name and can identify each command line argument. If we wanted to move into a directory called Holiday Photos for example the following would not work.

1. user@bash: ls Documents
2. FILE1.txt File1.txt file1.TXT Holiday Photos
3. ...
4. user@bash: cd Holiday Photos
5. bash: cd: Holiday: No such file or directory

What happens is that Holiday Photos is seen as two command line arguments. cd moves into whichever directory is specified by the first command line argument only. To get around this we need to identify to the terminal that we wish Holiday Photos to be seen as a single command line argument. There are two ways to go about this, either way is just as valid.

## Quotes

The first approach involves using quotes around the entire item. You may use either single or double quotes (later on we will see that there is a subtle difference between the two but for now that difference is not a problem). Anything inside quotes is considered a single item.


1. user@bash: cd 'Holiday Photos'
2. user@bash: pwd
3. /home/ryan/Documents/Holiday Photos

## Escape Characters

Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.

1. user@bash: cd Holiday\ Photos
2. user@bash: pwd
3. /home/ryan/Documents/Holiday Photos

In the above example the space between Holiday and Photos would normally have a special meaning which is to separate them as distinct command line arguments. Because we placed a backslash in front of it, that special meaning was removed.

## Hidden Files and Directories

Linux actually has a very simple and elegant mechanism for specifying that a file or directory is hidden. If the file or directory's name begins with a . (full stop) then it is considered to be hidden. You don't even need a special command or action to make a file hidden. Files and directories may be hidden for a variety of reasons. Configuration files for a particular user (which are normally stored in their home directory) are hidden for instance so that they don't get in the way of the user doing their everyday tasks.

To make a file or directory hidden all you need to do is create the file or directory with it's name beginning with a . or rename it to be as such. Likewise you may rename a hidden file to remove the . and it will become unhidden. The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.

1. user@bash: ls Documents
2. FILE1.txt File1.txt file1.TXT
3. ...
4. user@bash: ls -a Documents
5. . .. FILE1.txt File1.txt file1.TXT .hidden .file.txt
6. ...

In the above example you will see that when we listed all items in our current directory the first two items were . and .. If you're unsure what these are then you may wish to have a read over our previous section on Paths.

## Summary

### Stuff we Learnt

**file** 
obtain information about what type of file a file or directory is.

**ls -a**
List the contents of a directory, including hidden files.

### Important Concepts

**Everything is a file under Linux**
Even directories

**Linux is an extensionless system**
Files can have any extenstion they like or nome at all.

**Linux is case sensitive**
Beware of silly typos.


