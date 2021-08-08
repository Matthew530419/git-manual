###1. Git concept

- Git is not only Version Control System(VCS) but also Distributed Version Control(DVC)
  ![concept](./img/concept.png)
  ![concept](./img/concept1.png)

- Git workflow could be devided below
  ![workflow](./img/workflow.png)

- Git could restore file from commit to untracked on working directory.
  ![workflow](./img/checkout.png)

- Commit include hash code based on snapshot information and this help we could reference version. move file from staging area to .git directory with saving history
- Git could upload on remote storage
  ![workflow](./img/push.png)

- Git could download from remote storage
  ![workflow](./img/pull.png)

###2. Why use Git

- Most commonly used
- Free
- Open source
- All activities fast
- Work offline when server error
- Undo mistakes
- Easy and fast branching/merging
- Better cooperation with making branches per function

###3. Interpreting git commands

- `git config --list`: Show me all setting list
- `q`: exit and come back to terminal
- `git config --global core.editor "code"`: Setting on using terminal when executing vscode
- `git config --global core.editor "code --wait"`: Setting on using terminal when exiting vscode
- `git config --global -e`: Edit setting with vscode
- `code .`: Connection with vscode
- `git config --global user.name "Matthew530419"`: Setting user information for name
- `git config --global user.email "sprite530@naver.com"`: Setting user information for email
- `git config user.name`: Check user name
- `git config user.email`: Check user email
- `git config --global core.autocrlf input`: Change the line on OS(window or Mac) efficiently when using git repository
- `git init`: Initialize empty git repository
- `ls -al`: Check lists on current directory
- `rm -rf git`: Cancel git init
- `git status`: Check git status
- `git config --global alias.st status`: Use keyword instead of full sentence
- `git config --h`: Check help means command and option regarding configration
- `git status --h`: Check help means command and option regarding status
- `git status --s`: Show status concisely
- `git diff -h`: Check help means command and option regarding diff **why not --h?**
- `echo hello world! > a.txt`: make a.txt with "hello world!" sentence on untracked condition
- `echo style > style.css`: make style.css with "style" sentence on untracked condition
- `echo log > log.log`: make log.log with "log" sentence on untracked condition
- `echo *.log > .gitignore`: ignore all files with ".log" extension
  `echo build/*.log > .gitignore`: ignore all files with ".log" extension on "build" subdirectory
- `git add <file>`: moving file from untracked on working directory to staging area. `git add *` means all file move
- `git rm --cached <file>`: moving file from staging area to untracked on working directory
- `start .git`: open folder of named ".git" on window OS. If Mac OS, use `open .git`
- `git diff`: Compare with before and after on working directory. before means file on staging area "new file: " and after means file on tracked on working directory "modified: "
  ![diff](./img/diff.png)
  `--- a/a.txt` means before file condition
  `+++ b/a.txt` means after file condition
  `@@ -1 hellow world!` means look before file first line and check written down hellow world!
  `+1, 2 @@ +hi` means add another line and check written down hi, and then, total lines become 2 lines. +hi is green color because of adding
  If you diff file on staging area, use `git diff --staged` same ad `git diff --cached`
  ![diff](./img/diff1.png)
  `--- /dev/null` means no file before
- `cat a.txt`: All sentences in a.txt are displayed on terminal

###1. Normal opration

- `renamed:` means `git rm <filename>` and `git add <changed filename>`
  ![rename](./img/rename.png)

###2. failures

- Local image file was connected with Github. The file was in subdirectory named "img". This was changed information such as name, and then, git didn't recognized with this file and display deleted: when `git status`.
  I couldn't match between this file and git status, however, I found how to recognize this. That was moving this file to root directory. I don't know the reason why git can not recognize this file when any changed information in subdirectory.
