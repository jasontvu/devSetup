# preliminaries

$ which node        // find out if node is already installed
                    // if already installed, you may want to remove it
                    // cd into that directory and delete it
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt-get install build-essential lamp-server^
$ sudo mkdir -p ~/build/
$ ver=6.5.0         // replace this with the latest version available on nodejs.org
$ cd $HOME/Downloads
$ wget -c https://nodejs.org/dist/v$ver/node-v$ver.tar.gz     // this is to download the source code
$ sudo mv node-v$ver.tar.gz ~/build/
$ cd ~/build/
$ sudo chmod 777 -R .
$ tar -zxvf node-v$ver.tar.gz
$ cd node-v$ver
$ sudo chmod 777 -R .
$ sudo ./configure && sudo make && sudo make install
$ node -v
$ npm version
// Once installed, verify your installation:
$ node
>console.log('Hello');
>Hello
To exit, press CTRL+C twice

# install git & Ionic & Visual Studio Code
$ sudo apt-get install git
$ sudo npm install -g ionic@beta
// To update ionic:  $sudo npm update -g ionic
// To uninstall ionic:  sudo npm uninstall -g ionic
// Download Visual Studio Code .deb file to install
// the install Debugger for Chrome Code extension (ctl+shft+X)
// then select Chrome startup profile in Code
$ ionic info
$ ionic start githubIonic tutorial --v2 --ts            // Start new project: githubIonic with template: tutorial
$ ionic serve
$ ionic g page users    // generate a page called users



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
