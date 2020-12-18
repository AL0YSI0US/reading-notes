Git vs Github / local vs Remote / Clone / Commit / ACP / VCS / Deployment

## Reading Notes ##
:electron: [Git Master CHEAT](https://overapi.com/git)

[Git Tutorial](https://blog.udemy.com/git-tutorial-a-comprehensive-guide/#4_1)

[Git Community Book](http://alx.github.io/gitbook/)

[GUI Client Downloads] (https://git-scm.com/downloads/guis)

| ***States***| Files in Git can reside in three main states: committed, modified and staged. | 
|  :----: |  ----  |   
|   **Committed**  |  Data is securely stored in a local database  | 
|   **Modified**  |  File has been changed but not committed to the database  |
|   **Staged**  |  Flagged a file’s changed version to be committed in the next snapshot |

**There are three ways to get more information on a particular command, 
by accessing the manual:**

1. **git help** *command*

2. git *command* **--help**

3. **man git-** *command*

# Revisions and the Cloud

## blah blah



## Vocabulary

|**Term**|**Context**|  
|  :----: |  ----  |   
|   VCS  |  **Version Control** is a **system** that allows you to revisit various versions of a file or set of files by recording changes. Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.  | 
|   Local  |  Many years ago, programmers created **Local Version Control systems**. A Local VCS entails one database on your hard disk that stores changes to files.  |
|   CVCS  |  The need for collaboration within a developer team on a single file or set of files led to the advent of the **Centralized Version Control System (CVCS)**. This system entails a single server storing all changes and file versions, which can be accessed by various clients. This streamlined the collaboration process (by eliminating the need to involve all local databases), allowed programmers to have more knowledge of team members’ activities with certain files, and gave administrators much more control over divvying up revision privileges.  |
|  Remote Repositories  |  In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.  |
|  Cloned Repositories  |  As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.  |
|   Remote Clone  |  ----  |
|   ACP  |  ----  |
|   Deployment  |  ----  |

## Cloning ##
**You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:**

> $ git clone https://github.com/test  

By cloning the file, you have copied all versions of all files for a project. This command leads to the creation of a directory called “test,” with an initialized .git directory inside it, which has copies of all versions of all files for the specified project. The command also automatically checks out — or retrieves for editing — a copy of the newest version of the project.

**To clone a repository into a directory with another name of your choosing, use the following command format:**

> $ git clone https://github.com/test mydirectory 

The command above makes a copy of the target repository in a directory named “mydirectory.”


[Code 102 Table of Contents](CodeFellows_102.md)

[<== Home](README.md) [Forward ==>](html_markup_semantics_wireframe_personas_meta_content_element_tag_attribute_structure_vs_presentation.md)
