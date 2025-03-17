

Create a folder and open in VS code
Type "git log" message shown as fatal: not a git repository (or any of the parent directories): .git
Above message is because git is not initialized.
git init - Initializes and created .git
git status - Denotes Its on branch master & No commit in Git

git add index.html  -- Adds index.html to Staging in master branch.
git commit -m "Initial commit in Git"   - This commits index.html to the master branch.

git log --- Denotes the Commtis done.(Here one Commit)

Modifies one more time in index.html
git add index.html - Added index.html to Staging stage.
git commit -m "second time " Added one more commit..

git log -- Shows 2 commits..

Moving between commits in Local Git:
git checkout <firstcommitid>  -- Shows the First committed file . 
git status -- Head detached at master.

To move back to master branch.
git checkout master   (or)
git checkout <<seondcommitid>>

In Githib
Created a fresh GitHub repository namely githubcourse

Establish connection between Git and GitHub  - git remote add

git remote add origin https://github.com/privatesuyambu/githubcourse.git

In above command "origin" (can be any name) is the LocalIdentifier of the remote repository
It is the name of the remote github repository.

Now executing
git push , but error states that current branch master does not have any upstream branch.

git push  origin master
This pushes the Local Git master branch to the Colud repository master branch.

It happend because already connection establishes using Personal Access Token.
Ways to give Permission or Access between Git and GitHub
One way - git remote set-url origin https://privatesuyambu.github.com/privatesuyambu/githubcourse.git
Then give "git push origin master"  (It asks for Personal Acces TOken , give it)
Another way to establis strict connection between Local Git and Remote
git push --set-upstream origin master

Changed something in index.html
Then did git add & git commit in Local Git , It creates one more new commit.

Now did git push -- It pushes the latest commit to the GitHub Repository,

Same way add , commit and push , pushes to the master branch.

For feature branch :
git checkout -b featureone - This creates featureone branch and checkout immediately in Git

Now the pointer in featureone branch, Now change some content and do add and commit in the Feature branch.
My task is to move the local feature branch to Cloud.
git push origin featureone. - origin is the name of the cloud repository and featureone is the branch , by giving the command entire branch is moved from local to cloud.
Now successfully local feature branch featureone is moved to cloud with the same beanch name featureone.

Now the task is to merge featureone with main.
git checkout master  ---> Switches to branch master.
git merge featureone --->Now master is merged with featureone.

Now I need to push it to Cloud.
git push --> this command pushes the contents to master branch in the Cloud .Point to be noted is no separate commit required. It is due to merge command.

But if there are clashing conflicts then separate commit is needed.

Now featureone branch is deleted in cloud.
git branch -D featureone. --> To delete in local GIT.






