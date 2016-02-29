# Git and GitHub for Librarians

## Intro
Hi, I'm Megan! Today we're talking about Git and GitHub for Librarians (and Archivists, and Museum folk, etc.). You can use this outline to follow along with the workshop materials, and to refer back to in the future.

Specifically, here you'll find instructions for doing some basic work with Git or GitHub. So buckle in and let's get started :)

## Git
### Getting started: Opening the command line
#### Mac OS:
1. Open Launchpad OR open a finder window and go to "Applications"
2. Look for the program "Terminal" -- in Launchpad it's probably under "Other," in Finder > Applications it'll be under "Utilities"

#### Windows:
1. Open the Start menu and type `cmd` into the prompt; choose "cmd" from the options that appear

### Command Line Basics
Type the part of the text `that looks like this` for each command to try it out.

#### Mac OS:
1. Figure out what folder you're in: `pwd`
2. Find out what's in that folder: `ls`
3. Leave the Terminal for a moment and create a new folder on the Desktop as you normally would
4. Move into that folder using Terminal:
	* Click and drag the folder into your command line window
	* Use the back arrow to get to the beginning of the line and type `cd`
	* It should look like: `cd path/to/your/file`
5. Make a new folder inside that folder using the command line: `mkdir foldername.txt` *no spaces in the folder name!*
6. Make a new file: `touch filename.txt`

#### Windows:
1. Figure out what folder you're in: `echo %cd%`
2. Find out what's in that folder: `dir`
2. Leave the command prompt for a moment and create a new folder on the Desktop as you normally would
4. Move into that folder using cmd:
	* Change the current directory to the Desktop: `cd Desktop`
	* See what's on your Desktop: `dir`
	* Move into the right folder: `cd path\to\your\file`
5. Make a new folder inside that folder: `mkdir foldername` *no spaces in the folder name!*
6. Make a new file: `fsutil file createnew filename.txt 0`

### Git basics:
#### Mac OS:
1. Figure out what folder you're in: `pwd`
2. If applicable, go back up one directory: `cd ..`
3. Now that you're back in the folder you made on your Desktop in the last part of the instructions, make it a git repository: `git init`

#### Windows OS:
1. Figure out what folder you're in: `echo %cd%`
2. If applicable, go back up one directory: `cd ..`
3. Now that you're back in the folder you made on your Desktop in the last part of the instructions, make it a git repository: `git init`

#### Everybody:
4. You should now have an (invisible) file called .git that keeps track of your git changes!
5. To see what's happening with git and your files: `git status`
6. To add files to what git tracks: `git add filename` -- this "stages" your file(s)
7. To save the changes with a message: `git commit -m "your commit message"`

#### Reversing a change:
1. Updating the commit you just made (with one more change, etc.):
	* `git commit -m "initial commit"` 
	* Oops -- you realize you need to add one more file, make one more change to your CSS, etc.
	* Make changes
	* `git add forgotten_file.css`
	* `git commit --amend`
2. Un-staging a staged file (you stages a file before you realized you were done with it):
	* `git add filename.js`
	* `git status` will show that "filename.js" is under "Changes to be committed"
	* Realize you weren't done with "filename.js"
	* `git reset HEAD CONTRIBUTING.md`
	* `git status` should show that "filename.js" is under "Changes not staged for commit"

#### Making a branch:
1. To make a new branch: `git branch branchname`
2. To "move" to the branch: `checkout branchname`
3. To do both at once: `git checkout -b branchname`

## GitHub
