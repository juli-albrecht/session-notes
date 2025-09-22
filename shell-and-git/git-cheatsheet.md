# Basic Git Commands
## Create directories and navigate trough shell
- mkdir _filename_: Create directory 📁
- touch _filename.txt_: Create file (in this case text-file) 📄
- cd _filename_: Change directory to _filename_ 
- cd ..: Move one directory up 
- cd ~: Move to home directory
- tree: Tree-structure of directories and files in selected directory
- ls: List all directories and files in selected directory

## Move, delete and copy directories and files
- cp -R|--recursive _filename_: Copy directory/ file
- mv _filename_: Move directory/ file
- mv _filename, old_ _filename, new_: Change name of directory/ file
- rmdir _filename_: Delete empty directory
- rm -r|--recursive _filename_: Delete directory including contents

## Workflow to push to or pull from github
1. Create file with **touch _filename.txt_**
2. Open file in editor with **open .**
3. Edit file in editor and press cmd+s
4. Back in the terminal add file to stage with **git add**
5. Use **git commit -m "_description_"** to commit changes 
6. Push to git  
6.1 With **git push** to main branch  
6.2 With **git push -- set-upstream origin _branchname_** to new branch 
7. In Github: Click pull-request > Compare & Pull request to merge to main
8. In Terminal: **git pull** to synch changes from github to local 