# Git File Tracking Life Cycle
There are total four stages:
1. Untracked state : Files are present in the local directory, but not added in the github repository index.
2. Unmodified state : Files are already present in directory or added using $git add command. If some changes did, then it not get tracked. Also after commiting the      changes file status become unmodified.
3. Modified state : When previously tracked file is edited, but not commit the changes.
4. Staged state : When files committed and ready to push in git repository, then they have staged status.

This is very crucial for everyone to understand how files move and react on git's repository when you play around git-lab with command line interface. Let's understand it.

### How to find out the stage of Files that has/have been created/modified/updated/deleted?
#### Command :
> git status

### Example:
Let's say we have created a file called it as new_file.txt inside your git-lab directory.
### In Windows
#### Command :
> touch new_file.txt
or One can create manually via GUI.
### In Linux
#### Command:
> vi new_file.txt
##### Here Vi is a interactive advanced text editor for Linux User which let's you create files of any type via command line itself also provides you an environment to read/write content.

Now, The moment when we created this file; try running the command **Git status**. 
You will see output something like this:
```
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new-text.txt

nothing added to commit but untracked files present (use "git add" to track)
```
Now in order to change the stage of it. 
run this command.
### Command:
> git add new_file.txt
Again run the status command
> git status
See the output.
```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   new-text.txt

```

Now, you may see how the file moved from untracked to unstaged. 
Let's understand it, 
So, when we created the file that moment git was unaware of some sort it's existance whether it's related to the project or not. But, it knows that something new has been created and it's still not sure if we can keep it as part of the project or not. Now, The moment you tell git to add this file as part of the project by running **Git add** command then git is concluding okay now this no longer untracked.

Again, Let's make some changes to same file and run the **Git Status** command and you'll see below output. 
```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   new-text.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   new-text.txt
```
Now, Here we go for the definition of file modified stage.

Now when you commit the staged file to your git repo it attached as unmodified file and ready to push to git repo.
### run command:
> git commit -m "First commit"
```
$ git commit -m "First commit"
[master (root-commit) e75f6cb] First commit
 1 file changed, 2 insertions(+)
 create mode 100644 new-text.txt
```
> git status
```
$ git status
On branch master
Your branch is based on 'origin/master', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
```

Hope you understood the concept behind this file tracking system below is the final conclusion and some important git commands related to this.

![This is an image demonstrating file tracking system in git](https://git-scm.com/book/en/v2/images/lifecycle.png)

### Global config for git in your local environment.
>Git config --global user.name

>Git config --global user.email

### Basics commands
1. Git init **To start a new repository in your local environment**
>git init

2. Git clone **To clone new repository to your local environment**
>git clone

3. Git Add **To add newly created files/projects to git repository**
>git add <file-name/project-name>
>git add *  # To add entire directory/all files to push to the git reposiroty.

4. Git Commit
>git commit -m "message describing this commit" 

5. Git Diff
>git diff #post to commit when you made any changes to any file and run this command you'll see how it tracks the changes interactively.

6. Git Show
>git show # This will show the activity like /changes/modified/commited file status in hierarchy.

7. Git Push
>git push -orgin master # After committing all the unmodified files will be pushed to your git's repository.

8. Git Pull
>git pull # This will help you get the latest updated project available to your local environment.
