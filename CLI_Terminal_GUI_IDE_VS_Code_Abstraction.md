Update CLI / Terminal / GUI / IDE VS Code / Abstraction 
# The Coder's Computer

:electron: [THE LINUX CHEAT](https://overapi.com/linux) 

> The computer is a bicycle for the mind.
>
> —Steve Jobs

## Reading Notes ##

:mortar_board: [Choosing a text editor](https://codefellows.github.io/code-102-guide/curriculum/class-02/Choosing-A-Text-Editor--The-Older-Coder.pdf)

**Text Editor**

A text editor is a piece of software that you download and install on
your computer, or you access online through your web browser, that
allows you to write and manage text, especially the text that you write
to build a web site. The text editor has to be one of the most
important tools you can use as an aspiring web developer.

:mortar_board: [Linux Tutorial - 1. The Command Line](https://ryanstutorials.net/linuxtutorial/commandline.php)

:mortar_board: [Linux Tutorial - 2. Navigation](https://ryanstutorials.net/linuxtutorial/navigation.php)

:mortar_board: [Linux Tutorial - 3. More About Files](https://ryanstutorials.net/linuxtutorial/aboutfiles.php)

:mortar_board: [Linux Tutorial - 4. Manual Pages](https://ryanstutorials.net/linuxtutorial/manual.php)

**Everything is a file under Linux**

- Even directories.

**Linux is an extensionless system**

- Files can have any extension they like or none at all.

**Linux is case sensitive**

- Beware of silly typos.

|**command**|**result**| 
|  :----: | ---- |
|  **pwd** |  Print Working Directory - ie. Where are we currently.  | 
|  **cd** |  Change Directories - ie. move to another directory.  | 
|  **ls** |  List the contents of a directory.  | 
|  **ls -a** |   List the contents of a directory, including hidden files.  | 
|  **file** |  Obtain information about what type of file a file or directory is.  |
 |  **~(tilde)** | This is a shortcut for your ***home directory***. eg, if your home directory is /home/ryan then you could refer to the directory Documents with the path /home/ryan/Documents or ~/Documents |
 |  **.(dot)** | This is a reference to your ***current directory.*** eg in the example above we referred to Documents on line 4 with a relative path. It could also be written as ./Documents (Normally this extra bit is not required but in later sections we will see where it comes in handy). |
 |  **..(dotdot)** | This is a reference to the ***parent directory.*** You can use this several times in a path to keep going up the hierarchy. eg if you were in the path /home/ryan you could run the command ls ../../ and this would do a listing of the root directory. |

## Vocabulary

|**Term**|**Context**| 
|  :----: |  ----  |   
|   CLI  | **Command Line Interface** processes commands to a computer program in the form of lines of text. The program which handles the interface is called a command-line interpreter or command-line processor. Operating systems implement a command-line interface in a shell for interactive access to operating system functions or services. Such access was primarily provided to users by computer terminals starting in the mid-1960s, and continued to be used throughout the 1970s and 1980s on VAX/VMS, Unix systems and personal computer systems including DOS, CP/M and Apple DOS.| 
|   Terminal  | **Terminal.app** is the terminal emulator included in the macOS operating system by Apple. Terminal originated in NeXTSTEP and OPENSTEP, the predecessor operating systems of macOS. As a terminal emulator, the application provides text-based access to the operating system, in contrast to the mostly graphical nature of the user experience of macOS, by providing a command-line interface to the operating system when used in conjunction with a Unix shell, such as zsh (the default shell in macOS Catalina). The user can choose other shells available with macOS, such as the KornShell, tcsh, and bash. |
|   GUI  | The **Graphical User Interface** is a form of user interface that allows users to interact with electronic devices through graphical icons and audio indicator such as primary notation, instead of text-based user interfaces, typed command labels or text navigation. GUIs were introduced in reaction to the perceived steep learning curve of command-line interfaces (CLIs), which require commands to be typed on a computer keyboard. |
|   IDE  | An **Integrated Enviornment Development** (IDE) is a software application that provides comprehensive facilities to computer programmers for software development. An IDE normally consists of at least a source code editor, build automation tools and a debugger. Some IDEs, such as NetBeans and Eclipse, contain the necessary compiler, interpreter, or both; others, such as SharpDevelop and Lazarus, do not. The boundary between an IDE and other parts of the broader software development environment is not well-defined; sometimes a version control system or various tools to simplify the construction of a graphical user interface (GUI) are integrated. Many modern IDEs also have a class browser, an object browser, and a class hierarchy diagram for use in object-oriented software development.  |
|   Abstraction  |  **Abstraction** is the process of removing physical, spatial, or temporal details or attributes in the study of objects or systems to focus attention on details of greater importance; it is similar in nature to the process of generalization; the creation of abstract concept-objects by mirroring common features or attributes of various non-abstract objects or systems of study – the result of the process of abstraction.  |
| Absolute  |  (paths) A file or directory location in relation to the root of the file system.|
| Relative  |  (paths) A file or directory location relative to where we currently are in the file system.|

**Code Completion** 

allows you to start typing, and the code completion
feature will display possible suggestions based on what you originally
typed. This saves you time by providing a choice, rather than allowing
you to finish typing and possibly encounter typos.

## Every computer will come with its own text editor ##

On Mac computers, the text editor that comes with your computer is called,
“Text Edit.” On Windows computers, the text editor that comes with
your computer is called, “Notepad.”
And on Linux computers, each distribution will have its own text
editor already installed but which one might depend on the flavor of
your particular distribution. These text editors will go by different
names.

## Folder/ Extentions ##

Also, make sure that when you use the text editor that comes on your
computer, that you first create a folder on your computer somewhere
(maybe on your Desktop, for example) to store your entire website.
As you create new documents with the text editor that comes on your
computer, save those files in the appropriate folders or sub-folders
within the main website folder.
Also, please make sure that when you’re saving your file, that they
have the appropriate extension at the end of the file names. For
example, **your main HTML file should be called, “index.html.” Your
CSS file should be called something like “style.css.” The filename isn’t
as important as the extension (the “.html” and the “.css”).**



[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](git_vs_github_local_vs_remote_clone_commit_acp_vcs_deployment.md)
