
# Lab 2: Resizing Many Images Using a Shell Script

The purpose of this lab is to become familiar with how to combine your
knowledge of the available commands on a Unix system to create a script
of shell commands. Additionally, the lab will require the use of the git
utility.

## Goals
* Use Tuffix and become more familiar with the Unix system
* Clone a GitHub repository
* Install software on your Tuffix system, as needed
* Use the built-in commands in BASH to write a simple program using loops, conditions, and parameters
* Commit your edits and push your changes to the GitHub hosted repository

## Prerequisites
For this assignment, you must have:
* a GitHub account linked to your university email address
* a Tuffix system or VM

## Lab instructions

### Cloning the Git Repository

One you are logged into your GitHub account, open the assignment URL that your instructor has shared with you. (Most likely it will be on the class Titanium page.)

After opening that link, GitHub will generate the your own repository that will contain the starter code of the lab. This is the same repository where you will be pushing (submitting) your code for grading. Once the repository is generated, a similar message will show:

> Your assignment has been created here: https://github.com/csufcs-cpsc-254/cpsc254-lab-2-image-resize

Open the link to see the web-view of your GitHub repository.

Next clone your repository to your local computer so that you can start working. You are expected to add as many files as you need to complete this assignment. Only include your source code and do not add any data files. You can add files to your repository using the `git add` command.

To clone your repository, click on the **Clone or download** green button on the top right, and then click on the copy button right next to the repository address. Then, go back to the terminal and run the following command:

```
$ git clone [paste repository URL]
```

The command will ask you to input your GitHub username and password. Be aware that your password will not echo (show up) on the terminal; it will appear as though nothing is being typed.

### Create a Shell Script

Using your preferred text editor, create a new file and name it `quickresizer`. The script `quickresizer` shall take JPEG file names as parameters and resize the files. The rules of the script are that if the image is wider than 1024 pixels, it must be resized to be 1024 pixels wide and maintain the aspect ratio. If the image is less than 1024 pixels wide, then do not modify the image. Furthermore, ensure that the script is able to handle multiple files as parameters. For instance, if 100 files are given as parameters, then each file is processed.

Additionally, if the program is run without any parameters it prints out a usage message indicating the correct usage of the script. The usage message is like an online help message explaining to the user how to correctly invoke the script.

A collection of sample images is provided for you to use. The images are posted online on [Google Drive](https://drive.google.com/file/d/1nmEbRuYa2LsRs-TOm1lPtbgMgnNWL3NE/view?usp=sharing) as a zip archive.

Remember to add a hash-bang (`#!`) and include a header at the top of the file with your full name, email address, class, and section number. Include a brief one or two line description of the shell script and any software requirements the script has beyond what is included with Tuffix.

An example script is included, named `trivialexample` which demonstrates some good practices and a template for you to follow.

### Installing Software
You may find it necessary to install software on your system to complete the assignment. To do so, use the `apt-get` command with the `install` directive.

Command line image processing software is readily available. Two popular packages are Image Magick and Graphics Magick.

### Pushing code to Git (submitting your assignment)

To submit your code, you will need to add the files that you want to submit, commit your changes, and push them into the GitHub repository.

#### Adding the files

You can verify the status of the files in your repository by running `git status`. It will tell you if files have been modified or untracked. If a file is not tracked, then it will not be submitted. Make sure your script is added to your repository.

#### Committing changes

To commit your changes, you run the command `git commit -m "Some quick description here"`. The `-m` indicates that the next parameter will be a description of your commit. The description should always be a sentence explaining what your change is about, and should be readable and useful for other engineers/programmers to understand what your change did. Some examples of commit descriptions could be *"Fixed bug that was causing the camera app to crash."* or *"Implemented the search feature for the project."*

If you omit the `-m` option, a text editor will open and you may edit and save your comment through the editor. You can select your default editor by setting the `EDITOR` and `VISUAL` environment variables.

#### Pushing your commit to GitHub

The last step is to push (upload) your commit to GitHub. Using the `git push` command will upload your commits to your repository on GitHub. You can verify that your commit was successful by reloading the GitHub repository page to see your commit message and modifications.

You can also try re-cloning your repository to see exactly what the instructor will see when grading your assignment.

## Rubric (10 points)
1. (5 points) `quickresizer` operates correctly according to the specification
2. (2 points) The script is correctly named `quickresizer`
3. (2 points) The script has an appropriate header and help message

Assignments that are not submitted through GitHub shall not be graded.

