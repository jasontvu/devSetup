# devSetup

Basic development workflow

Always start every new development with blank repository on github.com 
and setup your pc to use your github account.  

In this example, let's create a github repository called devSetup.

$ git config --global user.email "jasontvu@mydshbrd.com"
$ git config --global user.name "jasontvu" (Jxxxxxxxxxxxxxxx!!)

On your pc, create a local repository under ~/build/repos and initial it.

$ cd ~/build/repos/
$ git init

Then clone the blank github repository into your local repository.

$ git clone https://github.com/jasontvu/devSetup.git

Now if you have another repository you want to clone into your local repository, then clone it also.

$ git clone https://gangachris/githubIonic.git

Then merge that new repository into your blank repository on your local pc.

$ sudo cp -R ~/build/repos/githubIonic/* ~/build/repos/devSetup/

Now from your local repository, tell git about the newly merged files.
$ git add .
$ git commit -a -m "added new files from githubIonic.git"

Do your development by editing/creating new files in your local repository.

When done, push them back to your github.com repository.

$ git push https://github.com/jasontvu/devSetup.git master

DONE