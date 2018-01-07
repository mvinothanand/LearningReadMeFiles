*******************************************************************************
Commands
*******************************************************************************
-------------------------------------------------------------------------------
Configuring Git
-------------------------------------------------------------------------------
git config
	> --global user.name mvinothanad --> This sets the user name against which the commits are recorded
	> --global user.email vinoth.anand@gmail.com --> this sets the email against which the commits are recorded
	> --list --> Lists all config variables and their values.
	> --<key> --> to find out the value set for a specified key.

-------------------------------------------------------------------------------
Getting help on Git Commands
-------------------------------------------------------------------------------
git help <verb>
	Example: git help -config

man git-<verb>

-------------------------------------------------------------------------------
Initializaing a repository
-------------------------------------------------------------------------------
1. Go to the directory 
2. git init

-------------------------------------------------------------------------------
Cloning an existing repository
-------------------------------------------------------------------------------
git clone <url>
	Example: git clone https://github.com/libgit2/libgit2

-------------------------------------------------------------------------------
Getting status of files in a repository
-------------------------------------------------------------------------------
git status

Getting short status
--------------------
git status --short 
[OR]
git status -s
	A --> Tracked and staged for next commit
	M --> Modified but not staged for next commit
	?? --> Untracked
	MM --> Modified staged and then modified

-------------------------------------------------------------------------------
Tracking new files for commit to repository
-------------------------------------------------------------------------------
git add <file name>
	Example: git add abc.java
	Example: git add *.java

-------------------------------------------------------------------------------
Ignoring files from tracking
-------------------------------------------------------------------------------
Add the file name patterns to .gitignore:

Example .gitignore file:
--Content starts next line--
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in the build/ directory
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
--Content ends previous line--

-------------------------------------------------------------------------------
Knowing the differences between files
-------------------------------------------------------------------------------
git diff <file name> --> Difference between the working and staged file.
git diff --staged <file name> --> Difference between the staged and committed files.

-------------------------------------------------------------------------------
Committing changes to Git
-------------------------------------------------------------------------------
git commit
	--> This will open the editor with the list of files staged for commit (all commented)
	--> Add any additional messages if you want
	--> Exiting the editor will make git execute the commit.
git commit -a
	--> This commit will include all the files including those which are not added to the staging area.

-------------------------------------------------------------------------------
Removing a file from Git
-------------------------------------------------------------------------------
rm <file name>
	--> This will remove the file from the repository and will no longer appear in the tracked files list.

-------------------------------------------------------------------------------
Renaming or moving a file
-------------------------------------------------------------------------------
git mv <file from> <file to>

-------------------------------------------------------------------------------
Viewing the commit history
-------------------------------------------------------------------------------
git log
	--> List all changes in reverse chronological order
git log --patch -2
[OR]
git log -p -2
	--> List the most recent 2 commits with the actual changes

Check https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History for more useful options.

-------------------------------------------------------------------------------
Adding a remote
-------------------------------------------------------------------------------
git remote add <Shortname> <URL>


