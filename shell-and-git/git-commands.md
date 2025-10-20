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

## Reading files

- cat _filename.txt_: Print all contents
- open _filename.txt_: Open file in the default editor

## Workflow to push to or pull from github

1. In the local `web-challenges` repository, make sure you are on the `main` branch.
2. Create a folder with the name of the session. For example, `mkdir css-basic`.
3. Navigate to the folder created in step 2 `cd css-basics`.
4. Once you are inside the folder, download the challenge (using the npx command).This creates a new folder belonging to that challenge.
5. Change into that folder, e.g. `cd css-basics-pink-box`.
6. Open that folder with Visual Studio Code `code .`. From here it's easiest to use the Visual Studio Code Terminal `CMD + J`
7. Switch to a new branch for this challenge, e.g. `git switch -c feature/css-basics-pink-box`.
8. Do an initial commit `git add .` `git commit -m "initial commit"`.
9. Work on the challenge. You can do some commits from time to time.
10. Once you have finished the challenge commit and push all changes to Github `git push -u origin feature/css-basics-pink-box`.
11. Open a browser and go to your Github repository. Create a new Pull Request.
12. Copy the URL from the browser and send it to a team member and ask for a review (if you like)
13. Merge the PR on Github and delete the feature branch.
14. In VS Code switch to the main branch `git switch main`.
15. Pull the changes from Github `git pull`.
16. Delete the local feature branch `git branch -d feature/css-basics-pink-box`.
17. Close VS Code and in your terminal change into the sessions folder. Repeat all steps with the next challenge.

## Create new branches

- git switch -c _branchname_: Creates new branch

## Branch Management and Merging

- git fetch: To check whether your local branches are up to date with the remote repository (by default: origin)
- git merge: To join two branches together (Make sure to run git fetch first if you want to merge a remote branch switch to the branch where you want to incorporate the changes run git merge <branchname>)
- git pull: You can use git pull to fetch changes from a remote repository and merge them into the current branch.
- git rebase: To join two branches together. In contrast to git merge, it doesn’t create a merge commit, which results in a cleaner git history. This strategy first applies all the changes of the branch we are rebasing to (the branch used after the rebase command). Then it applies the changes of the branch we are rebasing from (the current branch) on top of it commit by commit. To rebase, switch to the branch where you want to incorporate the changes use git rebase main to incorporate the changes from the main branch into the branch you switched to
